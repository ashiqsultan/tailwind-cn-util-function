# tailwind-cn-util-function
A util function to resolve tailwind classes

## How to
Run `npm install clsx tailwind-merge`

Create a cn.js or cn.ts file and add this code to use it elsewhere in your components

```
import { twMerge } from 'tailwind-merge'
import { clsx } from 'clsx'

export function cn(...args) {
  return twMerge(clsx(args))
}
```

## Usage
```
const TabHeaderItem = ({ classNameFromProps, isActive }) => {
  return (
    <button
      onClick={() => onClick(id)}
      className={cn(
        'border-b-2 border-slate-800', //baseclass
        classNameFromProps, // Will be solved
        { 'border-b-2 border-green-200': isActive } // Conditional class
      )}
    >
      <Icon size={20} strokeWidth={2} className="mr-1" />
      {label}
    </button>
  )
}
```

