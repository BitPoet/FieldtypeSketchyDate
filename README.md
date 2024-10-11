# FieldtypeSketchyDate
ProcessWire field that stores an imprecise date (full date, year+month or just month)

# Status

alpha - use at your own risk

# Description

This Fieldtype/Inputfield for the ProcessWire CMS provides basic capabilities to store
incomplete date values, i.e. you can enter full dates, but you can also just input
a year or year-month combination.

The notation is always yyyy-mm-dd (or yyyy-mm or just yyyy). You can configure the
separator char, which defaults to a slash (/), in the field settings.

## Searching

Fields of this type are of course searchable. If you search for a date of type 2024/03,
for example, it will find all dates that range from 2024/03/01 to 2024/03/31 and
all dates that were just entered as 2024/03.

## Limitations

- Only supports four-digit years. If you want to input years under 1000, add leading zeroes (0120).
- Negative years (BC) and years past 9999 are not supported.
- There is no validation (yet) whether the entered date is actually valid, thus you can
  enter 2024/13/55 without error.
- Separator char has to be configured separately for input and output (as two separate modules
  are involved. This may change in the future).

# ToDo

- Date validation
- Calendar UI
- Configure separator char for input and output at once

# License

Released under Mozilla Public License. See file LICENSE for details.
