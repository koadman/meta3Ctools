
## assembly workflow concept

0. TODO: remove PCR duplicates (which software?? Super Deduper?)
	+ Rationale: duplicates may artificially inflate kmer counts
1. adapter trim (SeqPurge? Trimmomatic?)
	+ Rationale: stray adapters have a tendency to break assemblies & generally add noise to the DBG
2. quality trim
	+ Rationale: low quality regions add noise to the DBG
3. snip reads at proximity ligation junctions
	+ Rationale: ligation junctions create DBG paths that should not exist
4. assemble (megahit)


## other design ideas

where possible, use named pipes to move data from one step to the next
this will reduce disk I/O and speed things up	
