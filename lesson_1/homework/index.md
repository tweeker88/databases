title|   first_name  |     last_name   | correspondence_language | birth_date |gender  |marital_status|country|postal_code|region     |city                        |street            |building_number|
-----| ------------- | ----------------|-------------------------|------------|--------|--------------|-------|-----------|-----------|----------------------------|----------------- |---------------|
Dr.  |	Danilo	     |Ambrosini  	   |IT                       |	1900-01-01|	Unknown|		      |   IT  |	21100	  |	          |Varese                      |	Via dolomiti  |	13            |
Mrs  |	Deborah	     |Thomas		   |                         |            | Female |		      |   GB  |	RH16 3TQ  |		      |Haywards heath              |	Cobbetts mead |	31            |
Herr |	Markus	     |Hönninge	       |DE                       |	1900-01-01|	Male   |		      |   DE  |	69493     |		      |Hirschberg an der bergstraße|	Breitgasse 5a |	              |
Mrs  |	Sheila	     |Spiller	       |EN                       |		      | Unknown|		      |   GB  |	TN6 1ST	  |East sussex|	Crowborough                |	Ghyll road    |               |
Mrs  |	Rosemary	 |Bailey	       |EN                       |		      | Unknown|		      |   GB  |	NR34 7SH  |	          |	Beccles                    |	Pepys avenue  |	24            |
Mr   |	G	         |Russell	       |EN                       |	1900-01-01|	Male   |		      |   GB  |	FK6 6BW   |	          |	Denny                      |	Leslie park   |	              |
Mr   |	Mark	     |Robins	       |EN                       |		      | Male   |		      |   GB  |	BS7 0EY	  |	          |Horfield                    |	Flat 6        |	              |
Mrs  |	Elaine	     |Thomson	       |EN                       |	1900-01-01|	Female |		      |   GB  |	NG24 3LL  |		      |Newark                      |	38 main street|               |
	 |  Mario 	     |Bartolucci	   |IT                       |	1900-01-01|	Male   |		      |   IT  |	60018     | Ancona    |	Montemarciano              |	Via dei larici|	23            |


1. Заменяем gender на связь, может быть null
2. Заменяем язык на связь, может быть null
3. Заменяем страну на связь, не может быть null
4. Всю инфу о проживании переносим в табличку location
5. Обращение выносим в справочник и делаем связь со страной


***title***

id   |  value    | country |
-----|-----------|---------|
1    | Dr        |    1    |
2    | Mrs       |    2    |
3    | Mr        |    2    |
4    | Herr      |    3    |

***language***

id   |  name    |
-----|----------|
1    | IT       |
2    | DE       |
3    | EN       |

***gender***

id   |  gender  |
-----|----------|
1    | male     |
2    | female   |

***country***

id   |  name  |
-----|--------|
1    | IT     |
2    | GB     |
2    | DE     |

***location***

id   | country| postal_code|region|city|street|building|
-----|--------|------------|------|----|------|--------|
1    | 1      |
2    | 2      |
3    | 3      |
4    | 2      |
5    | 2      |
6    | 2      |
7    | 2      |
8    | 2      |
9    | 1      |


***final***

first_name   | last_name| birth_date|marital_status|location|gender|language|
-------------|----------|-----------|--------------|--------|------|--------|
Danilo       |Ambrosini |1900-01-01 |       null   |    1   | 2    |    1   |
Deborah      |Thomas    | null      |       null   |    1   | 2    |    1   |
Markus       |Hönninge  |1900-01-01 |       null   |    1   | 2    |    1   |
Sheila       |Spiller   | null      |       null   |    1   | 2    |    1   |
Rosemary     |Bailey    | null      |       null   |    1   | 2    |    1   |
G            |Russell   |1900-01-01 |       null   |    1   | 2    |    1   |
Mark         |Robins    | null      |       null   |    1   | 2    |    1   |
Elaine       |Thomson   |1900-01-01 |       null   |    1   | 2    |    1   |
Mario        |Bartolucci|1900-01-01 |       null   |    1   | 2    |    1   |

