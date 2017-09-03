```zsh
# Clone the initial repository
git clone git@github.com:eerwitt/command-line-mystery.git
cd command-line-mystery

# Check the status to see if anything is already marked as new (shouldn't be)
git status

# Edit my solution file
subl solution.md

# Commit initial solution
git add solution.md
git commit -a

# Start reading the instructions
less instructions

# Check for clues in the mystery
cd mystery
grep CLUE ./crimescene

# Search for person with the Latte
grep Annabel ./people

# Knock on her door
less streets/Mattapan_Street
# Goto line in file using less: http://stackoverflow.com/questions/8586648/going-to-a-specific-line-number-using-less-in-unix
# in less type 173g
# Try different interviews
less interviews/interview-47246024

less interviews/interview-699607

# Checking for vehicle
less vehicles
# Search in less for vehicles starting with L337 and ending in 9
# in less /L337..9
# Check which are over 6'
# Katie Park
# Mike Bostock
# John Keefe
# Erika Owens
# Matt Waite
# Brian Boyer
# Al Shaw
# Miranda Mulligan
# Joe Germuska
# Jeremy Bowers
# Jacqui Maher

# Check which is male/female and get their names
egrep '((Katie Park)|(Mike Bostock)|(John Keefe)|(Erika Owens)|(Matt Waite)|(Brian Boyer)|(Al Shaw)|(Miranda Mulligan)|(Joe Germuska)|(Jeremy Bowers)|(Jacqui Maher))' ./people | grep '\tM\t' | cut -f1

# Limit down by membership
egrep -R '((Joe Germuska)|(Brian Boyer)|(Mike Bostock)|(Jeremy Bowers)|(John Keefe)|(Al Shaw)|(Matt Waite))' ./memberships

# (Jeremy Bowers)|(Brian Boyer)|(Mike Bostock)|(Matt Waite)
# Not MB, wrong car color
# Not MW, wrong car manufacturer
# Not BB, wrong car manufacturer
# JB, it is JB
```



raiprakash:mystery (master)$ grep "CLUE" crimescene
CLUE: Footage from an ATM security camera is blurry but shows that the perpetrator is a tall male, at least 6'.
CLUE: Found a wallet believed to belong to the killer: no ID, just loose change, and membership cards for AAA, Delta SkyMiles, the local library, and the Museum of Bash History. The cards are totally untraceable and have no name, for some reason.
CLUE: Questioned the barista at the local coffee shop. He said a woman left right before they heard the shots. The name on her latte was Annabel, she had blond spiky hair and a New Zealand accent.
raiprakash:mystery (master)$ grep "Annabel" people
Annabel Sun	F	26	Hart Place, line 40
Oluwasegun Annabel	M	37	Mattapan Street, line 173
Annabel Church	F	38	Buckingham Place, line 179
Annabel Fuglsang	M	40	Haley Street, line 176
raiprakash:mystery (master)$ head -n 173 streets/Mattapan_Street | tail -n 1
SEE INTERVIEW #9437737
raiprakash:mystery (master)$ cd interview
-bash: cd: interview: No such file or directory
raiprakash:mystery (master)$ cd interviews/
raiprakash:interviews (master)$ ls
interview-000296	interview-2058907	interview-38299069	interview-586668	interview-7998181
interview-00448418	interview-210355	interview-3871205 	interview-58910793	interview-8095917
interview-00502304	interview-218131	interview-3871242 	interview-5905106	interview-809922
interview-005702	interview-221039	interview-38899905	interview-591273	interview-812725
interview-00617019	interview-223913	interview-3917097 	interview-5993978	interview-81443363
interview-00805135	interview-2277882	interview-391811  	interview-60081985	interview-822576
interview-016463	interview-229443	interview-39481114	interview-604403	interview-8245680
interview-020337	interview-23167806	interview-39825862	interview-608607	interview-825165
interview-022751	interview-2326746	interview-40534453	interview-6093093	interview-82705993
interview-0234126	interview-23371263	interview-40610944	interview-618764	interview-831512
interview-02422821	interview-233800	interview-409731  	interview-6203192	interview-833367
interview-0251720	interview-2415821	interview-41553314	interview-628618	interview-838259
interview-03098229	interview-243703	interview-416243  	interview-63308519	interview-8387710
interview-0315125	interview-2481877	interview-41814745	interview-637657	interview-8402388
interview-03316077	interview-250112	interview-4204949 	interview-637928	interview-8421696
interview-034070	interview-253705	interview-42161907	interview-638121	interview-8464899
interview-0349327	interview-255531	interview-4223536 	interview-6417794	interview-84688694
interview-04393507	interview-25582311	interview-4225866 	interview-645385	interview-849256
interview-044492	interview-25834905	interview-42396365	interview-6553472	interview-85262552
interview-0462097	interview-259909	interview-4262657 	interview-65792229	interview-8531248
interview-049721	interview-2601508	interview-42934869	interview-659803	interview-856221
interview-05297663	interview-26373485	interview-4299898 	interview-66101490	interview-8586380
interview-06032377	interview-2642139	interview-4335306 	interview-66282920	interview-861780
interview-0613334	interview-27042476	interview-4366523 	interview-6643191	interview-862173
interview-066291	interview-27504937	interview-44533008	interview-67279454	interview-862717
interview-071537	interview-275706	interview-4463090 	interview-673985	interview-8631232
interview-0732631	interview-279087	interview-448086  	interview-676473	interview-86395001
interview-07497003	interview-280877	interview-45615686	interview-67790846	interview-865918
interview-0768255	interview-2834518	interview-457117  	interview-680549	interview-867999
interview-092423	interview-284560	interview-457451  	interview-6808205	interview-8700943
interview-0953437	interview-2846076	interview-466195  	interview-68195573	interview-87126591
interview-096267	interview-289524	interview-4673074 	interview-68488577	interview-871877
interview-102490	interview-290346	interview-46773428	interview-68764140	interview-879569
interview-109118	interview-291440	interview-47246024	interview-6884359	interview-8819490
interview-1108561	interview-2922290	interview-4735823 	interview-6894000	interview-891720
interview-114661	interview-29316965	interview-4765278 	interview-69170457	interview-896668
interview-11495001	interview-2939888	interview-476744  	interview-6933068	interview-9004767
interview-116803	interview-296128	interview-478217  	interview-699607	interview-901603
interview-11705111	interview-29680692	interview-48088300	interview-70067280	interview-901645
interview-11783660	interview-29741223	interview-48148020	interview-70199425	interview-90394637
interview-11817172	interview-2976680	interview-483817  	interview-703831	interview-904020
interview-1186827	interview-29838622	interview-485229  	interview-704443	interview-907126
interview-1205060	interview-2995681	interview-4950099 	interview-70458099	interview-9074626
interview-1250176	interview-301018	interview-4961376 	interview-7046684	interview-911451
interview-125204	interview-30259493	interview-496772  	interview-7066082	interview-91673757
interview-125271	interview-3049045	interview-498331  	interview-706620	interview-917210
interview-1269181	interview-305694	interview-499096  	interview-707438	interview-9185205
interview-1310392	interview-305949	interview-50168425	interview-708943	interview-920304
interview-13768464	interview-306616	interview-50291987	interview-7103823	interview-92391023
interview-13889608	interview-3074127	interview-504687  	interview-71186817	interview-92670500
interview-13920860	interview-3099757	interview-509105  	interview-71226767	interview-927642
interview-1395414	interview-312546	interview-5143029 	interview-71298441	interview-9332386
interview-141030	interview-3128999	interview-514793  	interview-7180973	interview-9346061
interview-14153840	interview-3140662	interview-52280505	interview-71993338	interview-93473333
interview-144873	interview-31635890	interview-528044  	interview-720268	interview-93696502
interview-14590717	interview-3201508	interview-529706  	interview-7254073	interview-938991
interview-147283	interview-322305	interview-53318557	interview-728181	interview-9408565
interview-15187437	interview-32365018	interview-535181  	interview-730123	interview-94126412
interview-15354942	interview-324389	interview-5372865 	interview-73035802	interview-9437737
interview-1536668	interview-325611	interview-538900  	interview-7305678	interview-944493
interview-155049	interview-32639981	interview-54026669	interview-73585672	interview-9446528
interview-1578206	interview-32712166	interview-541518  	interview-737609	interview-9501580
interview-159848	interview-331178	interview-5455315 	interview-7422077	interview-95095182
interview-16098538	interview-332596	interview-54619323	interview-74225310	interview-95601730
interview-1642421	interview-33399976	interview-54851634	interview-7469675	interview-9618669
interview-1643440	interview-340396	interview-549055  	interview-7541406	interview-9620713
interview-16889008	interview-34041151	interview-55382746	interview-75434722	interview-9651888
interview-17248453	interview-342393	interview-55410365	interview-755037	interview-9666149
interview-17343208	interview-34359897	interview-55435298	interview-75633580	interview-97043057
interview-174898	interview-344331	interview-55477243	interview-7580872	interview-9709892
interview-1767435	interview-34690644	interview-555536  	interview-77014856	interview-9711852
interview-17827186	interview-347303	interview-5581158 	interview-770439	interview-9712946
interview-179719	interview-351963	interview-55841398	interview-77135281	interview-9728756
interview-1811770	interview-353218	interview-55984022	interview-7791374	interview-97393699
interview-18193261	interview-353467	interview-565396  	interview-780255	interview-97409610
interview-1823688	interview-354262	interview-566707  	interview-7863761	interview-980963
interview-18270219	interview-3588302	interview-56784802	interview-789564	interview-982013
interview-18441251	interview-3609204	interview-56892213	interview-791289	interview-9824821
interview-1850922	interview-36398447	interview-57236791	interview-79360358	interview-98912259
interview-1857368	interview-364735	interview-5739404 	interview-79411932	interview-9901455
interview-1906958	interview-36527398	interview-5766907 	interview-794525	interview-9912172
interview-191206	interview-376115	interview-5774468 	interview-7959148	interview-992072
interview-19300543	interview-37747405	interview-5782759 	interview-796439	interview-99643550
interview-1933118	interview-3804339	interview-579105  	interview-79667499	interview-9969223
interview-19577850	interview-3824641	interview-5835471 	interview-79935965	interview-999372
raiprakash:interviews (master)$ cat interview-9437737
Doesn't appear to be the witness from the cafe, who is female.raiprakash:interviews (master)$ cd ..
raiprakash:mystery (master)$ ls
crimescene	interviews	memberships	people		streets		vehicles
raiprakash:mystery (master)$ grep -A 5 "L337" vehicles
License Plate L337ZR9
Make: Honda
Color: Red
Owner: Katie Park
Height: 6'2"
Weight: 189 lbs
--
License Plate L337P89
Make: Honda
Color: Teal
Owner: Mike Bostock
Height: 6'4"
Weight: 173 lbs
--
License Plate L337GX9
Make: Mazda
Color: Orange
Owner: John Keefe
Height: 6'4"
Weight: 185 lbs
--
License Plate L337QE9
Make: Honda
Color: Blue
Owner: Erika Owens
Height: 6'5"
Weight: 220 lbs
--
License Plate L337GB9
Make: Toyota
Color: Blue
Owner: Matt Waite
Height: 6'1"
Weight: 190 lbs
--
License Plate L337OI9
Make: Jaguar
Color: Blue
Owner: Brian Boyer
Height: 6'6"
Weight: 201 lbs
--
License Plate L337X19
Make: Fiat
Color: Blue
Owner: Al Shaw
Height: 6'5"
Weight: 240 lbs
--
License Plate L337539
Make: Honda
Color: Blue
Owner: Aron Pilhofer
Height: 5'3"
Weight: 198 lbs
--
License Plate L3373U9
Make: Ford
Color: Blue
Owner: Miranda Mulligan
Height: 6'6"
Weight: 156 lbs
--
License Plate L337369
Make: Honda
Color: Blue
Owner: Heather Billings
Height: 5'2"
Weight: 244 lbs
--
License Plate L337DV9
Make: Honda
Color: Blue
Owner: Joe Germuska
Height: 6'2"
Weight: 164 lbs
--
License Plate L3375A9
Make: Honda
Color: Blue
Owner: Jeremy Bowers
Height: 6'1"
Weight: 204 lbs
--
License Plate L337WR9
Make: Honda
Color: Blue
Owner: Jacqui Maher
Height: 6'2"
Weight: 130 lbs
raiprakash:mystery (master)$ cd memberships/
raiprakash:memberships (master)$ cat Museum_of_Bash_History  AAA Delta_SkyMiles Terminal_City_Library | grep -c "Jeremy Bowers"
4
Jeremy Bowers is the killer



