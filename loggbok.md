# Loggbok

## Vecka 1

Denna vecka började jag med att skapa ett repository och sätta upp rulesets för att begränsa vad användare kan göra i projektet. Exempelvis går det inte att pusha eller committa direkt till `main`, och varje merge måste granskas och godkännas av en annan användare i repot.

Därefter lade jag mycket tid på att hjälpa gruppen att få allting att fungera lokalt. Vi stötte på en del problem med att ge resterande gruppmedlemmar åtkomst till GitHub Packages, men efter lite felsökning fick vi det till slut att fungera.

Mot slutet av veckan skapade jag även en gemensam header och footer med länkar till projektets olika sidor.

**Problem och lösning:** Vi hade problem med åtkomst till GitHub Packages. Jag hjälpte gruppen att felsöka behörigheterna tills alla kunde köra projektet lokalt.

**Samarbete och agilt arbete:** Jag hjälpte gruppmedlemmarna att komma igång och bidrog med gemensamma komponenter som kunde användas av hela gruppen.

## Vecka 2

Denna vecka hade vi vår första ordentliga veckoplanering, där vi gick igenom hur arbetet skulle fördelas och vilka ansvarsområden som var rimliga utifrån svårighetsgrad och arbetsbelastning.

Därefter utvecklade jag en välkomstsida som visar den inloggade användarens användarnamn och roll. Jag lade även till skyddade routes för våra privata sidor. Dessa fungerar som en kontroll som ser till att endast autentiserade användare får tillgång till sidorna.

**Problem och lösning:** Det var viktigt att skilja på publika och privata sidor. Jag löste det genom att använda protected routes och kontrollera om användaren var inloggad.

**Samarbete och agilt arbete:** Vi planerade veckan tillsammans och fördelade uppgifter efter svårighetsgrad och arbetsbelastning.

## Vecka 3

Denna vecka började jag med att skapa en adminsida som endast användare med rollen `ADMIN` kan komma åt. Detta löste jag med hjälp av protected routes och en `requiredRole`-prop som kontrollerar om användaren har rätt behörighet. Det innebär att det inte räcker att vara inloggad, utan användaren måste även ha rätt roll.

Därefter lade jag till funktionalitet så att administratören kan se alla produkter som finns registrerade på sidan.

**Problem och lösning:** En användare skulle kunna vara inloggad utan att vara administratör. Jag löste det genom att även kontrollera användarens roll.

**Samarbete och agilt arbete:** Jag arbetade med en avgränsad uppgift från backloggen och kunde sedan visa resultatet för gruppen.

## Vecka 4

Jag började med att hämta alla kategorier och filtrera bort dubbletter så att varje kategori endast förekommer en gång i listan. Därefter skapade jag en funktion som listar kategorierna och visar alla produkter som tillhör den valda kategorin.

Det här var något nytt för mig eftersom jag tidigare inte hade använt `new Set()` för att ta bort dubbletter. Jag försökte därför dela upp arbetet i tre mindre delar för att göra lösningen så tydlig som möjligt:

1. Hämta och filtrera kategorierna.
2. Lista alla unika kategorier.
3. Visa produkterna som tillhör den valda kategorin.

Därefter lade jag till en sökfunktion så att användaren kan söka efter produkter på sidan. Jag använde React state för att spara produkterna och söka bland dem på klientsidan. På så sätt kan listan filtreras direkt medan användaren skriver. Med hjälp av `onChange` uppdateras sökfältets värde, som sedan används för att filtrera produkterna utifrån namn och beskrivning.

**Problem och lösning:** Det fanns dubbletter bland kategorierna. Jag löste det genom att använda `new Set()` innan kategorierna visades.

**Samarbete och agilt arbete:** Jag delade upp arbetet i mindre delar och arbetade stegvis, vilket gjorde det enklare att följa upp uppgiften.

## Vecka 5

Jag började med att gå igenom frontendens API-anrop och miljövariabler för att undersöka vad som behövde ändras för att använda en gemensam gateway-URL. Jag tittade även på vad som behövde förberedas kring CORS, JWT och authorization-headern.

Fokus låg på att få frontend och gateway att fungera tillsammans. Jag arbetade även med driftsättningen via min egen VPS (Virtual Private Server). Därefter kopplade jag DNS-inställningarna till VPS-serverns IP-adress för att kunna använda egna domäner vid driftsättningen.

**Problem och lösning:** Frontend och gateway behövde använda rätt URL och inställningar. Jag gick igenom miljövariablerna och kopplade DNS till VPS:ens IP-adress.

**Samarbete och agilt arbete:** Jag arbetade med en teknisk uppgift som stödde resten av gruppens funktioner och driftsättning.

## Vecka 6

Sjuk.

**Problem och lösning:** Jag var sjuk och kunde därför inte bidra som vanligt under veckan.

**Samarbete och agilt arbete:** Jag återupptog arbetet när jag kunde delta igen.

## Vecka 7

Jag var sjuk i början av veckan.

Senare under veckan arbetade jag med att konfigurera MSW och skapa en mockserver med tillhörande mockdata, bland annat exempeldata för användare och produkter.

Därefter skrev jag ett test för att kontrollera att hämtningen av produkter fungerade korrekt. Testet kontrollerar att datan som hämtas från mockservern stämmer överens med den förväntade mockdatan.

**Problem och lösning:** Det var svårt att testa API-anrop utan riktig backenddata. Jag löste det genom att använda MSW och mockdata.

**Samarbete och agilt arbete:** Jag bidrog med testning som gjorde det enklare för gruppen att upptäcka fel tidigt.

## Vecka 8

Denna vecka fokuserade jag på att finslipa hemsidan och förbättra dokumentationen i projektet. Jag lade till Javadoc-kommentarer för relevanta klasser och publika metoder.

Syftet var att göra det enklare för oss själva att förstå och vidareutveckla koden i framtiden. Det ska även underlätta för nya utvecklare att sätta sig in i projektet och förstå hur systemet fungerar.

**Problem och lösning:** Vissa delar av koden var svåra att förstå utan förklaring. Jag löste det genom att lägga till Javadoc för relevanta klasser och publika metoder.

**Samarbete och agilt arbete:** Jag förbättrade dokumentationen så att hela gruppen lättare kan förstå och vidareutveckla projektet.
