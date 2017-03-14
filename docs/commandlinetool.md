Helpinator comes with command-line compiler  **chelpinator.exe**  that you can use in batch files.


It has the following parameters:


**chelpinator.exe <format> <outputfileorfolder> [/v<variables.ini>] [/lang:LangID] <projectfile>**


<format> (required) - specifies output format. Can have the following values:


- /chm - for CHM format


- /rtf - for RTF format


- /pdf - for PDF format


- /html - for browser-based html help.


<outputfileorfolder> (required) - specifies full output folder or file name. Filename is for CHM, PDF and RTF formats and folder is for HTML format.


/v<variables.ini> (optional) - you can override values of project variables using this switch. Create a file with variables you want to override in the form:


VARIABLE=VALUE


For example:


VERSION=1.5.1


If the text after "/v" has no extension it is treated as variable preset name and the corresponding preset is selected.


/lang:LangID (optional) - one of project languages. Specify this parameter if you want to generate documentation for one of the languages in the project. LangID is required. You can find possible values in the following table:


LangID Language


0436 Afrikaans


041c Albanian


1401 Arabic (Algeria)


3c01 Arabic (Bahrain)


0c01 Arabic (Egypt)


0801 Arabic (Iraq)


2c01 Arabic (Jordan)


3401 Arabic (Kuwait)


3001 Arabic (Lebanon)


1001 Arabic (Libya)


1801 Arabic (Morocco)


2001 Arabic (Oman)


4001 Arabic (Qatar)


0401 Arabic (Saudi Arabia)


2801 Arabic (Syria)


1c01 Arabic (Tunisia)


3801 Arabic (U.A.E.)


2401 Arabic (Yemen)


042b Armenian


082c Azeri (Cyrillic)


042c Azeri (Latin)


042d Basque


0423 Belarusian


141a Bosnian (Latin, Bosnia and Herzegovina)


0402 Bulgarian


0403 Catalan


0c04 Chinese (Hong Kong S.A.R.)


1404 Chinese (Macau S.A.R.)


0804 Chinese (PRC)


1004 Chinese (Singapore)


0404 Chinese (Taiwan)


041a Croatian


101a Croatian (Bosnia and Herzegovina)


0405 Czech


0406 Danish


0465 Divehi


0813 Dutch (Belgium)


0413 Dutch (Netherlands)


0c09 English (Australia)


2809 English (Belize)


1009 English (Canada)


2409 English (Caribbean)


1809 English (Ireland)


2009 English (Jamaica)


1409 English (New Zealand)


3409 English (Philippines)


1c09 English (South Africa)


2c09 English (Trinidad)


0809 English (United Kingdom)


0409 English (United States)


3009 English (Zimbabwe)


0425 Estonian


042f FYRO Macedonian


0438 Faeroese


0429 Farsi


040b Finnish


080c French (Belgium)


0c0c French (Canada)


040c French (France)


140c French (Luxembourg)


180c French (Monaco)


100c French (Switzerland)


0456 Galician


0437 Georgian


0c07 German (Austria)


0407 German (Germany)


1407 German (Liechtenstein)


1007 German (Luxembourg)


0807 German (Switzerland)


0408 Greek


0447 Gujarati


040d Hebrew


0439 Hindi


040e Hungarian


040f Icelandic


0421 Indonesian


0410 Italian (Italy)


0810 Italian (Switzerland)


0411 Japanese


044b Kannada


043f Kazakh


0457 Konkani


0412 Korean


0440 Kyrgyz (Cyrillic)


0426 Latvian


0427 Lithuanian


083e Malay (Brunei Darussalam)


043e Malay (Malaysia)


043a Maltese


0481 Maori


044e Marathi


0450 Mongolian (Cyrillic)


046c Northern Sotho


0414 Norwegian (Bokmal)


0814 Norwegian (Nynorsk)


0415 Polish


0416 Portuguese (Brazil)


0816 Portuguese (Portugal)


0446 Punjabi


046b Quechua (Bolivia)


086b Quechua (Ecuador)


0c6b Quechua (Peru)


0418 Romanian


0419 Russian


243B Sami, Inari (Finland)


103b Sami, Lule (Norway)


143b Sami, Lule (Sweden)


0c3b Sami, Northern (Finland)


043b Sami, Northern (Norway)


083b Sami, Northern (Sweden)


203b Sami, Skolt (Finland)


183b Sami, Southern (Norway)


1c3b Sami, Southern (Sweden)


044f Sanskrit


0c1a Serbian (Cyrillic)


1c1a Serbian (Cyrillic, Bosnia and Herzegovina)


081a Serbian (Latin)


181a Serbian (Latin, Bosnia and Herzegovina)


041b Slovak


0424 Slovenian


2c0a Spanish (Argentina)


400a Spanish (Bolivia)


340a Spanish (Chile)


240a Spanish (Colombia)


140a Spanish (Costa Rica)


1c0a Spanish (Dominican Republic)


300a Spanish (Ecuador)


440a Spanish (El Salvador)


100a Spanish (Guatemala)


480a Spanish (Honduras)


0c0a Spanish (International Sort)


080a Spanish (Mexico)


4c0a Spanish (Nicaragua)


180a Spanish (Panama)


3c0a Spanish (Paraguay)


280a Spanish (Peru)


500a Spanish (Puerto Rico)


040a Spanish (Traditional Sort)


380a Spanish (Uruguay)


200a Spanish (Venezuela)


0441 Swahili


041d Swedish


081d Swedish (Finland)


045a Syriac


0449 Tamil


0444 Tatar


044a Telugu


041e Thai


0432 Tswana


041f Turkish


0422 Ukrainian


0420 Urdu


0843 Uzbek (Cyrillic)


0443 Uzbek (Latin)


042a Vietnamese


0452 Welsh


0434 Xhosa


0435 Zulu


<projectfile> (required) - full path to the Helpinator project you are about to compile.


Example.


Suppose path to your project is C:\Project\Help\myproject.hgu.


You need to compile PDF help from it and place it into C:\PDF folder. You have variable preset "pro" and want to use it. You have several languages in the project and you want to use "English (United States)"


You can use the following command line to do that:


chelpinator.exe /pdf /vpro /lang:0409 C:\PDF\myproject.pdf C:\Project\Help\myproject.hgu
