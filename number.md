// 数字使用千分位
function numberWithCommas(x) {
    return x.toString().replace(/\B(?<!\.\d*)(?=(\d{3})+(?!\d))/g, ",");
}

// Convert a number to a string with commas
function numberWithCommas(x) {
    return x.toString().replace(/\B(?=(\d{3})+(?!\d))/g, ",");
}

// Convert a number to a string with commas taking into account decimal point
function numberWithCommasDecimal(x) {
    return x.toString().replace(/\B(?<!\.\d*)(?=(\d{3})+(?!\d))/g, ",");
}

// result 3,000.00
Number(parseFloat(3000).toFixed(2)).toLocaleString('en', {
    minimumFractionDigits: 2
});

// result 123,233.12
Number(parseFloat(123233.12).toFixed(2)).toLocaleString('en', {
    minimumFractionDigits: 2
});
