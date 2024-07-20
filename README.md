## Ответы на тестовое [задание](https://plarson.ru/about/job/front-end/])

### Задание по разметке в файлах [index.html](./index.html) и [index.css](./index.css), а deploy [здесь](https://lodmevsimplemarkup.netlify.app/)

### SQL запрос для вывода месяцев и количества дней в них:
```sql
select MONTHNAME(MAKEDATE(year(curdate()), 1) + interval x.mon month) as Month,
DAYOFMONTH(LAST_DAY(MAKEDATE(year(curdate()), 1) + interval x.mon month)) as Days_quantity
from (select 0 as mon union all select 1 union all select 2 union all select 3 union all
      select 4 as mon union all select 5 union all select 6 union all select 7 union all
      select 8 as mon union all select 9 union all select 10 union all select 11
     ) x order by x.mon;
```
### JavaScript код аналогичный window.onload: 
```javascript
document.addEventListener('readystatechange', (event) => {
        if (event.target.readyState === 'loading') {
          console.log('Document loading...')
        }
        if (event.target.readyState === 'interactive') {
          console.log('Dom content loaded')
        }
        if (event.target.readyState === 'complete') {
          console.log('Loading complete')
        }
      })
```
