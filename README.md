### date-fns
---
https://github.com/date-fns/date-fns

```
npm install date-fns --save
yarn add date-fns
```

```js
import {format, compareAsc} from 'date-fns/esm'
format(new Date(2018, 11, 28), 'MM/dd/yyyy')
const dates = [new Date(1995, 6, 2), new Date(1987, 1, 11), new Date(1989, 6, 10)]
dates.sort(compareAsc)
```

```js
import { format, formatDistance, formatRelative, subDays } from 'date-fns'

format(new Date(), "Today is a' iiii")
formatDistance(subDays(new Date(), 3), new Date())
formatRelative(subDays(new Date(), 3), new Date())


import { formatRelative, subDays } from 'date-fns'
import { es, ru } from 'date-fns/locale'

formatRelative(subDays(new Date(), 3), new Date())

formatRelative(subDays(new Date(), 3), new Date(), { locale: es })

formatRelative(subDays(new Date(), 3), new Date(), { locale: ru })


import { addYears, formatWithOptions, toUpper } from 'date-fns/fp'
import { eo } from 'date-fns/local'

const addFiveYears = addYears(5)

const dateToString = formatWithOptions({ locale: eo }, 'D MMMM YYYY' )

const dates = [
  new Date(2017, 0, 1),
  new Date(2017, 1, 11),
  new Date(2017, 6, 2)
]

const toUpper = arg => String(arg).toUpperCase()

const formattedDates = dates.map(addFiveYears).map(dateToString).map(toUpper)
```

