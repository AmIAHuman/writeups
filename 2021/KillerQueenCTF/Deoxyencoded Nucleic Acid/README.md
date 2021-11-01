# Deoxyencoded Nucleic Acid
## Files
[`dna1.txt`](dna1.txt)
## Solution
| DNA | Binary |
| :-: | :----: |
|  A  |   00   |
|  T  |   01   |
|  G  |   10   |
|  C  |   11   |

DNA Sequence -> Binary -> UTF-8
### solve.py
```python
import binascii

seq = "TGGCTCATTGACTCTATGTGTCGCTGGTTCTATCACTTCCTGAGTGATTCACTGGTTGACTGATACATACATTCGTTTCCTGAGTGATTCACTGTTTTCCTGTGTGCCTCTTTCAGTCCT"

seq = seq.replace("A", "00")
seq = seq.replace("T", "01")
seq = seq.replace("G", "10")
seq = seq.replace("C", "11")

print(binascii.unhexlify('%x' % int(seq, 2)).decode('utf-8'))
```
```bash
$ python3 solve.py
kqctf{its_basica11y_base_four}
```
