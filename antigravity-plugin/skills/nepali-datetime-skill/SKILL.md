---
name: nepali-datetime-skill
description: Comprehensive knowledge on how to use the `nepali-datetime` node package. Use this when writing code that requires Nepali date conversion, formatting, or working with AD/BS calendars.
---

# `nepali-datetime` Skill

This skill provides the AI agent with the knowledge to write correct code using the `nepali-datetime` library.

## Overview

`nepali-datetime` is a robust Node.js library to handle Nepali dates (BS) and conversions between AD (Gregorian) and BS (Bikram Sambat).

## Imports

You can import the main class and the date converter as follows:

```typescript
// For NepaliDate and NepalTimezoneDate
import NepaliDate, { NepalTimezoneDate } from 'nepali-datetime'

// For date conversions
import dateConverter from 'nepali-datetime/dateConverter'
```

## Usage Examples

### 1. Working with NepaliDate

`NepaliDate` is a class similar to native JavaScript `Date` but strictly for the Bikram Sambat calendar.

```typescript
// Get the current Nepali date
const today = new NepaliDate()

// Parse a specific string
const specificDate = new NepaliDate('2080-01-01')

// Formatting
console.log(today.format('YYYY-MM-DD')) // Example output: '2080-01-01'
```

### 2. Using dateConverter

The `dateConverter` utility is perfect for AD to BS and BS to AD conversions.

```typescript
import dateConverter from 'nepali-datetime/dateConverter'

// Convert AD to BS
const bsDateString = dateConverter.adToBs('2023-04-14')

// Convert BS to AD
const adDateString = dateConverter.bsToAd('2080-01-01')
```

## Best Practices

- Always rely on `dateConverter` for straightforward string-based conversions rather than parsing it manually.
- Use `NepalTimezoneDate` when you specifically need the time accurately resolved to Nepal Time (NPT, UTC+5:45).
