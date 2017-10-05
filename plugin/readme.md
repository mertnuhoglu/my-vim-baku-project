
## Collecting review problems in a big review_tracking index file

Example:

	output:
		<url:file:///~/Dropbox (BTG)/TEUIS PROJECT 00-BTG TEAM FOLDER/problems/problem_rdb_review/problem_rdb_review_tracking.md>
	inputs:
		<url:/Users/mertnuhoglu/Dropbox (BTG)/TEUIS PROJECT 00-BTG TEAM FOLDER/problems/problem_rdb_review/problem_rdb_review_tracking.md#tn=## RDB Reviews>

How to do it?

1. review dosyasını aç
	üüy

2a. PutProblemId at the end of each problem
	@:
2b. PutProblemId2 at the start of each problem

input:

	p087: bazı enum'lar için enumvalue tanımlanmamış: 1, 12, 13, 14, 15, 28.

output:

	p:#p087: bazı enum'lar için enumvalue tanımlanmamış: 1, 12, 13, 14, 15, 28.

3. CopyProblemLines 

	run inside review_omer_xxx.md
	
	1. Put problem list into "a
		p:#p087: ...
		p:#p088: ...
	2. Put backreferences into "b
		r:review_omer_rdb_problemler_20160303.md#p087
	3. Paste "a and "b into problem_rdb_review_tracking.md

The references uses: Utl_AddressScheme_p

	1. "scope" kolonunu tüm "operations" kayıtları için dolduralım. p:#p070

Backreference uses: Utl_AddressScheme_r

	r:review_omer_rdb_problemler_20160303.md#p070

4. Build progress states table

	run inside problem_rdb_review_tracking.md

	:ConvertProblemList2TableOfStates

5. Jump from p003 to its Utl reference

	üüi :JumpToCorrespondingUtl

