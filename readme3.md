
export default (content) => {
  const array = content.split('\r\n');
  const bbb = array.slice(1, array.length - 1);
  console.log(Количество автомобилей: ${bbb.length});
  const car = bbb.map((r) => r.split(','));
  const probeg = car.map((r) => r[4]);
  const num = probeg.map((r) => Number(r));
  const nnn = _.sum(num);
  console.log(Средний пробег: ${nnn / bbb.length});
  const fira = car.map((r) => r[7]);
  console.log(Стоимость самой дорогой машины: ${_.max(fira)});


import _ from 'lodash';

export default (content) => {
  const rows = content.trim().split('\n').slice(1).map((row) => row.split(';'))
  console.log(Count: ${rows.length})

  const string = _.uniq(rows.map((el) => el[3])).sort();
  console.log(Currency codes: ${string.join(', ')});

  const minCost = _.min(rows.map((el) => Number(el[4])))
  const maxCost = _.max(rows.map((el) => Number(el[4])))
  console.log(Cost of currency: Min: ${minCost}, Max: ${maxCost});
}

import _ from "lodash";
export default function solution(content) {
  const array = content.split('\n').slice(1).map((row) => row.split(' '))
  console.log(Count: ${array.length});

  const castles = _.uniq(array.map((el) => {
    const res = el[1].charAt(0).toUpperCase() + el[1].slice(1).toLowerCase();
    return res;
  })).sort();
  console.log(Castles: ${castles.join(', ')});

  const largesthd = _.maxBy(array, (el) => Number(el[4]));
  console.log(Largest hp: ${largesthd[2]});
}

import _ from "lodash";
export default (content) => {
  const array = content.split('\r\n');
  const bbb = array.slice(1, array.length - 1);
  console.log(Количество автомобилей: ${bbb.length});
  const car = bbb.map((r) => r.split(','));
  const probeg = car.map((r) => r[4]);
  const num = probeg.map((r) => Number(r));
  const nnn = _.sum(num);
  console.log(Средний пробег: ${nnn / bbb.length});
  const fira = car.map((r) => r[7]);
  console.log(Стоимость самой дорогой машины: ${_.max(fira)});
  Количество автомобилей: 20
  Средний пробег: 30300
  Стоимость самой дорогой машины: 85000
}
