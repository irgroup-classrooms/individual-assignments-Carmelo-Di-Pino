# Data Cleaning and Analysis

## Data Fields

### `lotr_characters.csv`
- **race**: Race (e.g., Men, Orcs, Dragons).
- **death**: Death date (e.g., "February 26, 3019").
- **hair**: Hair description.
- **height**: Height (mostly missing).
- **name**: Character name.
- **gender**: Gender of the character.
- **realm**: Realm they belong to (e.g., Arnor).
- **spouse**: Name of their spouse, if any.
- **birth**: Birth date (e.g., "TA 2978").

### `lotr_scripts.csv`
- **char**: Character speaking the line.
- **dialog**: Dialog spoken by the character.
- **movie**: Movie in which the dialog appears (e.g., "The Return of the King").

## Cleaning Steps

### `lotr_characters.csv`
1. Dropped rows where `name` was missing.
2. Standardized column names to lowercase.
3. Trimmed whitespace from text fields.

### `lotr_scripts.csv`
1. Removed redundant index column.
2. Dropped rows with missing or empty `char` and `dialog` fields.
3. Standardized column names to lowercase.
4. Trimmed whitespace from `char` and `dialog` fields.

## Analysis

### Total Number of Lines and Unique Words in Dialogs
- **Total Lines**: 2,389
- **Unique Words**: 3,327

Commands:
```bash
wc -l lotr_scripts_cleaned.csv  # Counts the number of lines.
cat lotr_scripts_cleaned.csv | grep -oE '\w+' | sort | uniq | wc -l  # Counts unique words.
```

### Distribution Across the Three Movies
- **The Two Towers**: 1,010 lines
- **The Return of the King**: 873 lines
- **The Fellowship of the Ring**: 506 lines

Commands:
```bash
cut -d',' -f3 lotr_scripts_cleaned.csv | sort | uniq -c  # Counts occurrences of each movie.
```

### Top 5 Characters in `char`
- **Frodo**: 226 lines
- **Sam**: 217 lines
- **Gandalf**: 205 lines
- **Aragorn**: 187 lines
- **Pippin**: 163 lines

Commands:
```bash
cut -d',' -f1 lotr_scripts_cleaned.csv | sort | uniq -c | sort -nr | head -5  # Top characters.
```

### Top 5 Characters in Dialogs
- **Gandalf**: 3,254 words
- **Sam**: 2,287 words
- **Frodo**: 1,864 words
- **Aragorn**: 1,489 words
- **Gollum**: 1,442 words

Commands:
```bash
cut -d',' -f1,2 lotr_scripts_cleaned.csv | grep -oE '\w+' | sort | uniq -c | sort -nr | head -5  # Top dialogue counts.
```
