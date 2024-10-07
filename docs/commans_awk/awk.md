# C O M M A N S - A W K


### Basic Syntax

```sh
awk '{print $0}' file.txt # Print each line of the file

awk '/pattern/ {print $0}' file. txt # Print lines that match the pattern

awk '{print $1}' file.txt # Print the first column of each line

awk '{print $1, $3}' file.txt # Print the first and third columns of each ine

awk 'BEGIN {print "Header"} {print $0} END {print "Footer"}' file.txt # Add a header and footer
```

### Field and Record Separators

```sh
awk -F":" '{print $1}' /etc/passwd # Use ":" as the field separator, print the first field

awk 'BEGIN {FS=":"} {print $1}' /etc/passwd # Set ficld separator ":" in the BEGIN block

awk 'BEGIN {RS="\n\n"} {print $6}' file.txt # Use an empty line as the record separator
```

### Pattern Matching

```sh
awk '$3 ~ /pattern/ {print $6}' file.txt # Print lines where the third field matches a pattern

awk '$3 I~ /pattern/ {print $6}' file.txt # Print lines where the third field does not match a pattern
```

### Arithmetic Operations

```sh
awk '{print $1 + $2}' file.txt # Add the first and second fields of each Line

awk '{sum += $1} END {print sum}' file.txt # Sun the values of the first field across all ines

awk '{avg = ($1 + $2 + $3)/3; print avg}' file.txt # Calculate the average of the first three fields
```

### Conditional Statements

```sh
awk '{if ($1 > 50) print $6}' file.txt # Print Lines where the first field is greater than 50

awk '$1 > 5 {print $0}' file. txt # Alternative syntax for the same condition

awk '{if ($1 > 50) print "High"; else print "Low"}' file.txt # Print "High" or "Low" based on the first field
```

### Working with Multiple Files

```sh
awk 'FNR==1 {print "Processing " FILENAME}' filel.txt file2.txt # Print a message when starting a new file

awk 'FNR==NR {suml += $1; next} {sum2 += $1} END {print suml, sum2}' filel.txt file2.txt # Separate calculations for each file
```

### Text Processing

```sh
awk '{gsub(/pattern/, "replacement", $0); print}' file.txt # Replace all occurrences of "pattern" with "replacement"

awk '{print toupper($0)}' file.txt # Convert each line to uppercase

awk '{print tolower($0)}' file.txt # Convert each line to lowercase
```

### Output Redirection

```sh
awk '{print $1}' file.txt > output.txt # Redirect output to a file

awk '{print $1}' filel.txt >> output.txt # Append output to a file
```

### Working with CSV Files

```sh
awk -F"," '{print $1, $3}' file.csv # Print the first and third columns from a CSV file

awk 'BEGIN {FS=","; OFS=";"} {print $1, $3}' file.csv # Change output field separator to ";" ## Associative Arrays

awk '{count[$1]++} END {for (word in count) print word, count[word]}' file.txt # Count occurrences of each word in the first field
```