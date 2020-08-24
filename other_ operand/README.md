# Operand

代數運算子用來進行日常的十進位代數運算。包括以下運算子：

+：相加
-：相減
*：相乘
/：相除
%：取餘數
以下是簡短範例：

```
#include <assert.h>

int main(void)
{
    assert(4 + 3 == 7);
    assert(4 - 3 == 1);
    assert(4 * 3 == 12);
    assert(4 / 3 == 1);
    assert(4 % 3 == 1);

    return 0;
}
```

許多 C 語言教材會用 printf 將資料輸出終端機，但我們刻意用 assert 巨集檢查運算結果是否正確。因為透過 assert 巨集可自動檢查程式是否正確，但使用 printf 函式得手動檢查。而且 assert 敘述可以表明我們的意圖。

除了上述運算子，還有遞增和遞減運算子：

++
--
遞增、遞減運算子會帶著隱性的狀態改變，在使用時要注意。以下是範例：

```
#include <assert.h>

int main(void)
{
    unsigned n = 3;

    assert(++n == 4);
    assert(n++ == 4);
    assert(n == 5);

    return 0;
}
```

在這個範例中，第一個 assert 敘述使用 ++n，會先加 1 再比較值。但第二個 assert 敘述使用 n++，會先比較值才加 1。

由於遞增、遞減運算子會造成隱性的狀態改變，應儘量把敘述寫簡單一些，以免發生預期外的結果。