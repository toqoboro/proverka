# proverka
import _ from 'lodash';

export default (content) => {
  // Write your code here
const arr = content.split('\r\n');

let a = arr.slice(1, arr.length - 1);
console.log(a);
console.log(`Count: ${a.length}`);
//number 1 
const map = a.map(rrr => rrr.split(`;`))
const n = map.map(r => r[4])
const max = _.max(n)
const min = _.min(n)
console.log(`Cost of currency: Min: ${min}, Max: ${max}`);
//number 2 
const m = map.map (rrr => rrr[3])
const saxar = _.sortBy(m);
const sol = _.uniq(saxar);
console.log(`Currency codes: ${sol.join(', ')}`);
//number 3
let count2 = 0;

for (let i = 1; i < arr.length; i++) {
  const rate = parseFloat(arr[i].split(';')[4]);
  if (rate >= 10 && rate <= 30) {
    count2++;
  }
}

console.log(`Count currency between 10 and 30: ${count2}`);
//number 4 
}

1. Вывести на экран количество переданных значений. Например,
2. Вывести список кратких описаний валют отсортированных в алфавитном порядке
3. Найти в представленном наборе данных минимальное и максимальное значение
4. Вывести на экран количество валют, стоимость которых лежит в диапозоне от 10 до 30 (включительно)
```bash
Count: 31
Cost of currency: Min: 0.0595924, Max: 95.8018
Currency codes: AMD, AUD, AZN, BGN, BRL, BYN, CHF, CZK, DKK, EUR, GBP, HKD, HUF, JPY, KRW, SEK, USD, ZAR
Count currency between 10 and 30: 5
Arithmetic mean for USD, EUR, CHF is 56
