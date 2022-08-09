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

// 保留小数位数, 四舍五入还是截断
function round (number, decimals, truncate) {
    if (truncate) {
        number = number.toFixed(decimals + 1);
        return parseFloat(number.slice(0, -1));
    }

    var n = Math.pow(10.0, decimals);
    return Math.round(number * n) / n;
};
