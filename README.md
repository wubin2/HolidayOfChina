# HolidayOfChina
Holiday Of China API, [Example](https://api.coolsong.com/today.php). 
Updated 2025 holidays.

### GET dayInfo
URL
```
https://api.coolsong.com/calendar/day/20221210
```
#### Return Data
```
{
    "ok": true,
    "data": {
        "isRestDay": true,
        "isWeekend": true,
        "desc": "周末"
    }
}
```
***
### GET monthRestDays
URL
```
https://api.coolsong.com/calendar/monthrestdays/202107
```
#### Return Data
```
{
    "ok": true,
    "data": {
        "totalRest": 9,
        "restDays": [
            {
                "date": "20210703",
                "desc": "周末"
            },
            {
                "date": "20210704",
                "desc": "周末"
            },
            {
                "date": "20210710",
                "desc": "周末"
            },
            {
                "date": "20210711",
                "desc": "周末"
            },
            {
                "date": "20210717",
                "desc": "周末"
            },
            {
                "date": "20210718",
                "desc": "周末"
            },
            {
                "date": "20210724",
                "desc": "周末"
            },
            {
                "date": "20210725",
                "desc": "周末"
            },
            {
                "date": "20210731",
                "desc": "周末"
            }
        ],
        "totalWorkOnWeekend": 0,
        "workButWeekend": [

        ]
    }
}
```
***
### POST workingdays
URL
```
https://api.coolsong.com/calendar/workingdays
```
Headers
```
Content-Type : application/json
```
Body
```
{
    "start": "20210101",
    "end": "20211231"
}
```
#### Return Data

```
{
    "ok": true,
    "data": {
        "workingDay": 250,
        "weekEnd": 104,
        "publicRestDay": 18,
        "weekendButWorkingDay": 7
    }
}
```
***
### POST endDay
URL
```
https://api.coolsong.com/calendar/endday
```
Headers
```
Content-Type : application/json
```
Body
```
{
    "start": "20210727",
    "days": 2
}
```
#### Return Data

```
{
    "ok": true,
    "data": {
        "endDate": "20210728",
        "workingDay": 2,
        "weekEnd": 0,
        "publicRestDay": 0,
        "weekendButWorkingDay": 0
    }
}
```
***
