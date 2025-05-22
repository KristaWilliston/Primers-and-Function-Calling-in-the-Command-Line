import sys
primers = sys.argv[1]
seq = sys.argv[2]

primer = ''.join(open(primers).read().split())

# DNA Sequence
#primer = 'TCGCCTCGACTCCAAATGG'

# function complement returns complementary nucs
def complement(nuc):
    nucleotides = 'ACGT'
    complements = 'TGCA'
    i = nucleotides.find(nuc)
    if i >= 0:
        comp = complements[i]
    else:
        comp = nuc
    return comp

# function reverse_complement returns reversed and complemented primers
def reverse_complement(primers):
    reverse_comp = '' # empty string to build reverse complement by concatenating nucs
    for nuc in primers: # iterate through sequence
        reverse_comp = complement(nuc) + reverse_comp  # add nucs to beginning of string instead of end of string
    return reverse_comp

# reverse of the primer 
def reverse(primers):
    newseq = ""
    for nuc in primers:
        newseq = nuc + newseq
    return newseq

# Output the primers and nucs of reverse_complement
if seq == 'complement':
    print('Complement:',reverse(reverse_complement(primer)))
elif seq == 'reverse_complement':
    print("Reverse Complement:",reverse_complement(primer))
elif seq == 'reverse':
    print("Reverse:",reverse(primer))
else:
    seq
