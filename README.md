# Dokumentation för Skolprojekt i Python med Pandas #

## Syfte med projektet ##

Detta projekt syftar till att ge en analys av olika ekonomiska och fastighetsrelaterade data i Sverige. Genom att sammanställa och jämföra data om konsumentprisindex (KPIF), fastighetsindex, arbetslöshetsnivåer och bostadsrättspriser, ger projektet insikter i ekonomiska trender, bostadsmarknadens utveckling och arbetsmarknadens tillstånd över tid. Projektets mål är att möjliggöra för användare att visuellt jämföra dessa olika dataserier genom diagram.

## Datakällor ##
Data för detta projekt har hämtats från flera pålitliga källor för att säkerställa noggrannhet och relevans:

KPIF (Konsumentprisindex med fast ränta) och fastighetsindex data har inhämtats från Statistiska centralbyrån (SCB).

Arbetslöshetsdata har erhållits från Arbetsförmedlingen. Här var jag tvungen att rensa ur datan direkt ur excel och skicka över till en ny fil då den innehöll väldigt många kolumner med data och detta var det snabbaste och effektivaste sättet. Även om jag hade kunnat använda Pandas för detta. 

Bostadsrättspriserna har samlats in från Svensk Mäklarstatistik, en organisation som tillhandahåller detaljerad och uppdaterad statistik över bostadspriser och transaktioner i hela landet. Denna statistik har jag använt mig av mycket tidigare i mitt arbete som Fastighetsmäklare och har hög tillförlitlighet då statistiken är automatiskt inrapporterad från alla mäklare i Sverige. Fick ladda ner datan och föra över i annan excelfil att arbeta med och räkna ut 2023-års värde manuellt då det inte var sammanställt än av någon anledning. 

## Funktionalitet ##
Projektet erbjuder följande huvudfunktionaliteter genom en terminalbaserad meny:

Visning av Data: Användare kan välja att visa statistik för en enskild dataserie, inklusive KPIF, fastighetsindex, arbetslöshet och bostadsrättspriser. Varje dataserie visas som ett diagram, vilket ger en visuell representation av datans utveckling över tid.

Jämförelse av Data: Användare har möjlighet att jämföra två valfria dataserier sida vid sida. Detta görs genom att plotta de två valda serierna på samma diagram med dubbla y-axlar för att tydligt visa relationer och trender mellan dataserierna.

## Användarinstruktioner ##
För att använda programmet, följ dessa steg:

Starta Programmet: Kör huvudscriptet. Detta öppnar en terminalbaserad meny med flera alternativ.

Välj Funktion: Använd menyn för att välja om du vill visa en enskild dataserie eller jämföra två serier. Följ sedan instruktionerna på skärmen för att göra dina val.

### "plot_dataframe()" ###
Returnerar en plottad Dataframe när man väljer endast en Dataframe att titta på.

### get_dataframe_choice() ###
Returnerar en sträng av menyvalet som användaren gjort. Denna används för att få reda på vilka Dataframes som användaren vill jämföra.

### compare_dataframes() ###
Tar in två Dataframe-val som argument och plottar sedan dessa med två y-axlar och returnerar en plot på två Dataframes i samma plot.

### main() ###
Huvudfunktionen med en while-loop som körs hela tiden tills vi väljer "Q" för att avsluta loopen. Här finns huvudmenyn printad för användaren att se vad den kan välja. 
Returnerar menyn och plottar enligt önskemål på den datan som går att välja. 

Avsluta Programmet: När du är klar, välj alternativet "Q" för att avsluta programmet från huvudmenyn.

## Tekniska Förutsättningar ##
Projektet är utvecklat i Python och använder biblioteken Pandas för datahantering och Matplotlib för datavisualisering. För att köra projektet krävs Python samt installation av dessa bibliotek och användning av Jupyter Notebook. Där kan det vara olika beroende på vilken IDE man kör om man behöver installera något paket eller ej. Jag har använt mig av Anaconda och därigenom Jupyter Notebook direkt via Jupyter och inte via Pycharm då jag föredrar layouten och visualiseringen i Jupyter för dessa typer av projekt. 

## Framtid och Utveckling ##
Framtida versioner av projektet kan inkludera ytterligare dataserier, förbättrad interaktivitet och möjlighet till djupare analyser, såsom trendlinjer, prognoser och korrelationsanalys mellan olika dataserier. Tanken är att jag innan slutgiltlig inlämning ska göra en prognos på KPIF och Arbetslöshetsdata där jag har mycket data i form av månadsdata från 90-talet. 
