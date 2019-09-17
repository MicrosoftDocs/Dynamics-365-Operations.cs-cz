---
title: Konfigurace integrace mezd mezi aplikacemi Talent a Dayforce
description: Toto téma vysvětluje, jak nakonfigurovat integraci mezi aplikacemi Microsoft Dynamics 365 for Talent a Ceridian Dayforce pro zpracování výplat.
author: andreabichsel
manager: AnnBe
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: c26dfed9909b0dbd05fc18c206e5adc947feaef5
ms.sourcegitcommit: 45f8cea6ac75bd2f4187380546a201c056072c59
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/12/2019
ms.locfileid: "1742902"
---
# <a name="configure-the-payroll-integration-between-talent-and-dayforce"></a>Konfigurace integrace mezd mezi aplikacemi Talent a Dayforce

[!include [banner](includes/banner.md)]

Integrace mezi aplikacemi Microsoft Dynamics 365 for Talent a Ceridian Dayforce závisí na několika krocích konfigurace popsaných v tomto tématu. Před zpracováním výplat je nutné nakonfigurovat integraci v aplikaci Talent i Dayforce.

Pokud používáte službu, jako je Dayforce, pro dokončení zpracování výplat, je nutné povolit integraci v aplikaci Talent. Integrace vyžaduje specifická data z aplikace Talent. Z tohoto důvodu musí ověřit, zda data, která jsou mapována do Dayforce, jsou v aplikaci Talent nakonfigurována tak, aby podporovala integraci. Integrace používá následující rozsáhlé kategorie dat:

- Data lidských zdrojů
- Data kompenzací
- Mzdová data, jako například mzdové cykly, mzdová období a kódy příjmů
- Data pracovníka

Toto téma popisuje postup, který je třeba provést při povolení integrace. Vysvětluje také typy dat a podrobnosti konfigurace, které vyžaduje integrace.

## <a name="enable-the-integration"></a>Povolení integrace

V aplikaci Talent musíte zapnout integraci a zadat informace o konfiguraci pro připojení k aplikaci Dayforce. Pokud chcete, aby transakce hlavní knihy, která byla vytvořena, byla naimportována do aplikace Microsoft Dynamics 365 for Finance and Operations, musíte také nastavit účet úložiště Microsoft Azure a zadat řetězec připojení Azure Storage v aplikaci Finance and Operations.

Pro zapnutí integrace v aplikaci Talent postupuje podle těchto kroků.

1. Na stránce **Správa systému** zvolte **Konfigurace integrace**.
2. Zadejte koncový bod zabezpečeného FTP a cestu složky zabezpečeného FTP.
3. Zadejte uživatelské jméno a heslo uživatele, který bude mít přístup ke koncovému bodu zabezpečeného FTP a cesty ke složce.
4. Otestujte připojení podle potřeby a nastavte možnost **Povolit integraci mezd** na **Ano**.

Když je integrace zapnutá, vytvoří se balíček exportu dat a soubory, a nastaví se frekvence. Tuto frekvenci lze změnit v případě potřeby.

Další informace o účtech úložiště Azure a řetězcích připojení úložiště Azure Storage naleznete v následujících tématech Azure:

- [O účtech úložiště Azure Storage](https://docs.microsoft.com/azure/storage/common/storage-create-storage-account?toc=%2fazure%2fstorage%2ffiles%2ftoc.json)
- [Konfigurace řetězců připojení Azure Storage](https://docs.microsoft.com/azure/storage/common/storage-configure-connection-string)

### <a name="technical-details-when-payroll-integration-is-enabled"></a>Technické podrobnosti při povolení integrace mezd

Zapnutí integrace mezd má dva primární efekty:

- Je vytvořen projekt exportu dat s názvem "Export integrací mezd". Tento projekt obsahuje entity a pole vyžadované pro integraci mezd. Chcete-li zkontrolovat projekt, přejděte na položky **Správa systému**, vyberte dlaždici **Správa dat** a poté otevřete datový projekt ze seznamu projektů.
- Tato dávková úloha spustí projekt exportu dat, zašifruje výsledný balík dat a přenese soubor datového balíku do koncového bodu SFTP nakonfigurovaného na obrazovce **Konfigurace integrace**.

> [!NOTE]
> Datový balík převedený na koncový bod SFTP je šifrován pomocí klíče, který je pro daný balík jedinečný. Klíč je v úložišti klíčů Azure, který je přístupný pouze společnosti Ceridian. Není možné dešifrovat a prověřit obsah balíčku dat. Potřebujete-li zkontrolovat obsah balíčku dat, je třeba exportovat datový projekt integrace mezd ručně, stáhnout jej a poté jej otevřít. Ruční export nebude používat šifrování nebo nepřenese balíček.

## <a name="configure-your-data"></a>Konfigurace vašich dat 

Pro zpracování mezd je nutné konfigurovat data lidských zdrojů v aplikaci Talent. Musíte nastavit organizační data, například práce a pozice, včetně zaměstnaneckých výhod a informací o kompenzacích. Tyto informace poskytují informace o zaměstnání, mzdě a srážkách, které jsou nutné, pro vygenerování mzdy zaměstnance.

### <a name="human-resource-data"></a>Data lidských zdrojů

#### <a name="benefits"></a>Zaměstnanecké výhody 

Lidské zdroje poskytují nástroje pro natavení a správu zaměstnaneckých výhod, srážek a plánů kompenzace pracovníků, které organizace nabízí nebo zpracovává pro své zaměstnance.

Při vytváření zaměstnaneckých výhod mějte na paměti následující data a konfigurace, které se používají v Dayforce.

##### <a name="benefit-plans"></a>Plány zaměstnaneckých výhod

- Plán (povinný)
- Typ (povinný)
- Dopad mzdy (povinný)
- Obnovit nedoplatky
- Způsobu provádění odpočtu
- Priorita odpočtu
- Období limitu
- Částka limitu

##### <a name="benefits"></a>Zam. výhody

- Plán (povinný)
- Typ (povinný)
- Možnost (povinná)
- ID zaměstnanecké výhody (povinné)
- Četnost
- Základ
- Částka nebo sazba
- Kód příjmů

##### <a name="supported-frequencies"></a>Podporované intervaly 

- Týdně
- Čtrnáctidenně
- Každých 14 dní
- Měsíčně

##### <a name="supported-bases"></a>Podporované základy 

- Pevná částka
- Procento příjmů
- Produktivní hodiny

Dayforce vytvoří následující srážky, na základě dopadu mzdy, definovaného pro plán zaměstnaneckých výhod.

| Výběr v aplikaci Talent        | Výsledek v aplikaci Dayforce                            |
|----------------------------|-----------------------------------------------|
| None                       | Nebyla vytvořena žádná srážka.                      |
| Jen odpočet             | Byla vytvořena srážka zaměstnance.             |
| Jen příspěvek          | Byla vytvořena srážka zaměstnavatele.             |
| Odpočet a příspěvek | Jsou vytvořeny srážky zaměstnance a zaměstnavatele. |

Další informace o tom, jak definovat a spravovat program zaměstnaneckých výhod naleznete v následujících tématech:

- [Definování programu zaměstnaneckých výhod](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/deliver-employee-benefits-program)
- [Vytvoření nové zaměstnanecké výhody](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/create-new-benefit)
- [Definování pravidel a zásad nároků na zaměstnanecké výhody](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-benefit-eligibility-rules-policies)
- [Registrace a odebrání zaměstnaneckých výhod pracovníků](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-remove-benefits-workers)

#### <a name="compensation"></a>Kompenzace 

Správa kompenzací se používá k řízení doručení základní mzdy a odměn. Fixní základní mzda zaměstnance a nárůst odměn za zásluhy jsou řízeny prostřednictvím plánů fixní kompenzace. Pobídkové platby, jako například výplaty bonusů, výkonnostních odměn, opcí na nákup akcií nebo grantů, a také jednorázové odměny jsou řízeny prostřednictvím plánů variabilní kompenzace.

Dayforce používá informace o kompenzaci k výpočtu hodinové nebo roční sazby zaměstnance. Plány fixní kompenzace a převody mzdové sazby jsou povinné. Zaměstnanci musí být přiřazeni k plánu fixní kompenzace.

Další informace o plánech kompenzace naleznete v následujících tématech:

- [Vytvoření plánů fixní kompenzace](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-fixed-compensation-plans)
- [Vytvoření plánů variabilní kompenzace](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-variable-compensation-plans)
- [Vývoj struktury platu/kompenzace a plánů](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/develop-salary-compensation-structure-plan)
- [Proces kompenzace](https://docs.microsoft.com/dynamics365/unified-operations/talent/process-compensation)
- [Definování procesu kompenzací a výpočet výsledků](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-compensation-process-calculate-results)
- [Přihlášení zaměstnance k plánu fixní kompenzace](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-fixed-compensation-plan)
- [Přihlášení zaměstnance k plánu variabilní kompenzace](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-variable-compensation-plan)

#### <a name="jobs"></a>Práce 

Úloha je kolekce úkolů a odpovědností, které jsou vyžadovány od osoby, která provádí práci. Další informace naleznete v následujících tématech:

- [Nastavení komponent práce](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-job)
- [Definování nových pracovních míst](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-jobs)

##### <a name="positions"></a>Pozice

Pozice je individuální instance práce. Například pozice „Manažer prodeje (východ)“ je jednou z pozic, které jsou přidruženy k práci „Manažer prodeje“. Pozice existuje v oddělení. Ke každé pozic lze přiřadit pouze jednoho pracovníka.

Mějte na paměti následující data a konfiguraci při vytváření pozic:

- Pozice (povinná)
- Popis (povinný)
- Práce (povinná)
- Oddělení (povinné)
- Typ pozice (povinný)
- Ekvivalent plného úvazku
- Roční normální hodiny (povinné)
- Placené právnickou osobu (povinné)
- Platební cyklus (povinný)
- Výchozí finanční dimenze – Nákladové středisko (povinné)
- Přiřazení pracovníka – pracovník, začátek přiřazení, konec přiřazení, kód důvodu

Pokud je více pracovních pozic ve stejném oddělení přidruženo ke stejné práci, jsou sloučeny do jedné pozice v aplikaci Dayforce.

Další informace naleznete v následujících tématech:

- [Uspořádání zaměstnanců podle oddělení, prací a pozic](https://docs.microsoft.com/dynamics365/unified-operations/talent/departments-jobs-positions#positions)
- [Nastavení pozic](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/set-up-positions)

#### <a name="departments"></a>Oddělení

Oddělení je provozní jednotka, která představuje kategorie nebo funkční oblasti organizace. Oddělení je zodpovědný za určitou oblast organizace, jako například prodej, účtování nebo lidské zdroje. Oddělení můžete použít k sestavování funkčních oblastí. Oddělení mohou mít odpovědnost ze zisků a ztrát.

Další informace naleznete v následujících tématech:

- [Vytvoření oddělení a jeho přidružení k hierarchii oddělení](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-department-add-department-hierarchy)
- [Definování nových oddělení](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-departments)

#### <a name="pay-cycles-and-pay-periods"></a>Platební cykly a platební období

Platební cyklus určuje, jak často se zpracovává výpočet mzdy, a konkrétní dny výplaty pracovníků. Například platební cyklus může být měsíční a zaměstnanci mohou dostávat mzdu poslední den v měsíci. Popřípadě může být platební cyklus týdenní a zaměstnanci dostanou mzdu v úterý po ukončení platebního období. Platební cykly jsou přiřazeny k pozicím pro řízení dnů, kdy jsou pracovníci na těchto pozicích vypláceni.

Po vytvoření platebního cyklu lze generovat platební období pro každý cyklus. Každé platební období zahrnuje výchozí datum platby, které je založeno na informacích, které zadáte. Můžete však změnit výchozí datum platby v platebním období, abyste mohli povolit výjimky, například když datum platby spadá do prázdnin.

Následující informace se používají v aplikaci Dayforce:

- Platební cyklus (povinný)
- Četnost platebního cyklu (povinná)
- Počáteční datum období (první platební období je povinné)
- Výchozí datum platby (první platební období je povinné)

Tyto informace jsou integrovány s aplikací Dayforce jako platové skupiny a jsou oddělené podle země nebo oblasti pro každý platební cyklus. Před integrací musí být vytvořeno nejméně jedno platební období. Dayforce generuje kalendáře platebních skupin a data plateb na základě data zahájení prvního platebního období a výchozího data platby nastaveného v aplikaci Talent.

#### <a name="earning-codes"></a>Kódy příjmů

Kódy příjmů jedinečným způsobem identifikují každý typ příjmu, který zaměstnanci dostávají. Kódy mají různé parametry, které souvisejí s příjmy, například účetní pravidla, daňové předpisy, požadavky na vykazování a funkci hrubé mzdy.

Následující informace se používají v aplikaci Dayforce:

- Kód příjmů (povinný)
- popis
- Měrná jednotka
- Produktivní

### <a name="worker-data"></a>Data pracovníka

Záznamy o různých typech pracovníků, které máte, jsou důležité pro vaše lidské zdroje a mzdové systémy. Zadané informace lze použít ke sledování pracovníků a osobních informací.

Pro zaměstnance lze spravovat následující informace:

- **Základní** – Správa základních informací o pracovníkovi, jako jsou kontaktní informace, demografické informace, identifikační údaje, informace o rodině, stav vojenské služby, informace o cizincích a osobní a nouzové kontakty.
- **Zaměstnání** – Správa informací o pracovním poměru pracovníka, jako je například společnost nebo organizace, přidělení pozice, počáteční a konečné datum, způsobilost k práci, podmínky zaměstnání, důchod, dovolená a informace o přemístění.
- **Pracovní volno a absence** – Správa informací o absencích pracovníka, jako jsou pracovní kalendáře, transakce absencí a nastavení absencí.
- **Kompenzace a mzda** – Správa informací o plánech kompenzací pracovníka a mzdě, jako jsou registrace k plánu, odměny, výkonnost, provize, daňové informace, důchod a srážky z platu.

Při zadávání informací o pracovníkovi mějte na paměti následující data a konfigurace, které se používají v Dayforce.

#### <a name="general-information"></a>Obecné informace

- Osobní číslo (povinné)
- Jméno (povinné)
- Příjmení (povinné)
- Druhé jméno
- Datum služebního věku
- Známé jako

#### <a name="personal-information"></a>Osobní údaje

- Rodinný stav (povinný)
- Datum narození (povinné)
- Pohlaví (povinné)
- Osoba s tělesným postižením
- Země nebo oblast národnosti (pouze pro Mexiko)

#### <a name="address-information"></a>Informace adresy

- Primární (povinné)
- Země/oblast (povinné)
- PSČ (povinné)
- Číslo ulice (povinné) (pouze pro Mexiko)
- Doplňující název budovy (pouze pro Mexiko)
- Město (povinné)
- Stát (povinný)
- Okres (povinný)

#### <a name="contact-information"></a>Kontaktní informace 

- Primární (povinné)
- Kontaktní číslo (povinné)
- Linka

#### <a name="payroll-information-and-earning-codes"></a>Informace o mzdě a kódy příjmů

Zaměstnancům mohou být přiděleny konkrétní příjmy v konkrétním intervalu plateb a preferovaná metoda platby. Následující pole se používají v aplikaci Dayforce k zajištění, že toto se použijí tato nastavení a předvolby.

##### <a name="earning-codes"></a>Kódy příjmů

- Pozice (povinná)
- Kód příjmů (povinný)
- Frekvence (povinná)
- Částka (povinná)

##### <a name="payroll-information"></a>Mzdové informace

- Způsob platby
- Ekonomická oblast (povinná)
- ID zaměstnaneckých výhod
- Národní číslo ID (povinné)
- Číslo vojenské služby
- ID směny (povinné)
- Daňové číslo (povinné)
- ID odborů (povinné)
- ID pracovního dne (povinné)
- Číslo pracovního povolení

> [!NOTE]
> Ohledně metody platby podporuje Mexiko **Hotovost**, **Šek** (fyzický šek společnosti) a možnost **Electronické platby**. Pokud není metoda platby určena, používá se ve výchozím nastavení **Šek**.

#### <a name="employment-details"></a>Podrobnosti o zaměstnání

Historie detailů zaměstnání se používá jako klíčová informace pro odvozování stavu náboru zaměstnance, ukončení a opětovného náboru v aplikaci Dayforce. Dayforce podporuje vždy jen jeden aktivní záznam zaměstnání.

- Počáteční datum zaměstnání (povinné)
- Koncové datum zaměstnání
- Datum zahájení
- Upravené počáteční datum
- Datum ukončení zaměstnání (povinné při ukončení)
- Důvod ukončení zaměstnání (povinný při ukončení)

Klíčová data zaměstnance se odvozují pomocí následujících informací.

| Talent                | Dayforce                                                                                             |
|-----------------------|------------------------------------------------------------------------------------------------------|
| Datum posledního náboru | Začátek zaměstnání aktuálního záznamu historie bez ukončení zaměstnání                                 |
| Datum výpovědi      | Datum ukončení zaměstnání aktuálního záznamu historie bez ukončení zaměstnání                                 |
| Datum zahájení            | Upravené počáteční datum, datum zahájení nebo začátek zaměstnání současného neaktivního záznamu historie zaměstnání |
| Datum původního přijetí    | Začátek zaměstnání nejdřívějšího záznamu historie zaměstnání                                               |

#### <a name="compensation"></a>Kompenzace

Plán fixní kompenzace musí být přiřazen ke každé primární pozici zaměstnance v průběhu období zaměstnání. Toto období začíná v den, kdy byl zaměstnanec přijatý (nebo počátečním datem zaměstnání), a pokračuje až do ukončení pracovního poměru.

- Datum platnosti (povinné)
- Datum konce platnosti
- Mzdová sazba (povinná)
- Převody mzdové sazby (povinné)
- Roční ekvivalent (povinný)
- Hodinový ekvivalent (povinný)

Pokud má zaměstnanec s hodinovou mzdou více pozic, fixní kompenzace primární pozice se importuje do aplikace Dayforce jako základní sazba/plat na úrovni zaměstnance. U neprimárních pozic se hodinová sazba uloží k příslušné pozici v aplikaci Dayforce.

Pokud má zaměstnanec s platem více pozic, kumulativní hodinová sazba a roční plat na všech aktivních pozicích se odvozují a používají jako základní sazba/plat na úrovni zaměstnance.

#### <a name="identification-numbers"></a>Identifikační čísla

##### <a name="social-security-identifier"></a>Identifikátor sociálního pojištění 

Každý zaměstnanec musí mít jeden primární identifikátor. Tento identifikátor musí být typ identifikace **SSN**. V aplikaci Dayforce se automaticky odvozuje jako identifikátor sociálního pojištění zaměstnance, který se vyžaduje při náboru.

- Primární (povinné)
- Typ identifikace = SSN
- Datum vydání
- Datum vypršení platnosti

Zaměstnanec může deklarovat více identifikačních čísel typu identifikace **SSN**. Avšak pouze záznam, který je označen jako **Primární**, je integrován do Dayforce, bez ohledu na to, zda je číslo aktivní nebo s ukončenou platností.

#### <a name="bank-accounts-and-disbursements"></a>Bankovní účty a úhrady

Platné informace o bankovním účtu musí být zadány pro každého zaměstnance, který se rozhodne být vyplácen prostřednictvím bankovních převodů.

| Talent                         | Dayforce                                                                                                    |
|--------------------------------|-------------------------------------------------------------------------------------------------------------|
| Číslo bankovního účtu (povinné) |                                                                                                             |
| Kód SWIFT (povinný)          | Pole **ID banky** použité při zpracování mzdy v Mexiku.                                                             |
| Číslo pobočky (povinné)       |                                                                                                             |
| Typ bankovního účtu (povinné)   | Pole **Typ účtu** použitý při zpracování mzdy v Mexiku. Podporované hodnoty jsou **Běžný** a **Mzdový**. |

> [!NOTE]
> Zaměstnanci, kteří se rozhodnou být placeni prostřednictvím převodů na bankovní účet, musí poskytnout odkaz na zůstatkový účet, který je pod právnickou osobou s primární adresou v Mexiku a je spojen s platným bankovním účtem od mexické banky. Jiné než zůstatkové účty budou ignorovány.

#### <a name="address-information"></a>Informace adresy

Každý zaměstnanec musí mít jedno primární místo. V Dayforce toto místo slouží k určení primárního pobytu daného zaměstnance pro daňové účely.

- Primární (povinné)
- Země/oblast (povinné)
- PSČ (povinné)
- Ulice (povinná)
- Číslo ulice (povinné)
- Doplňující název budovy
- Město (povinné)
- Stát (povinný)
- Okres (povinný)

## <a name="configure-your-data-to-generate-payroll-in-united-states-and-canada"></a>Konfigurace dat pro generování mzdy v USA a Kanadě

Když generujete mzdu pro zaměstnance v USA a Kanadě, musí být nakonfigurovány následující prvky:

- Pro pozice jsou požadována oddělení.
- Nákladová střediska musí být nastavena jako finanční dimenze a musí být prvním prvkem ve výchozím řetězci finanční dimenze.

> [!NOTE] 
> Aplikaci Talent lze konfigurovat tak, aby od pozic požadovala určení oddělení. Chcete-li to provést, přejděte na **Sdílené pozice lidských zdrojů > Pozice > Vyžadovat oddělení na pozicích**. Doporučujeme, aby toto nastavení bylo vynuceno pro integraci.

### <a name="job-types"></a>Typ úloh

Typy prací se používají pro seskupení podobných pozic do kategorií. Typy prací jsou povinné pro zpracování mezd v USA a Kanadě. Příklady typů prací zahrnují plný úvazek a částečný úvazek, nebo plat a hodinovou mzdu. Typy prací jsou mapovány do Dayforce jako typy mezd, které označují, zda je zaměstnanec vyplácen hodinově nebo mzdou.

Následující typy práce a popisy jsou povinné.

| Typ práce   | Popis |
|------------|-------------|
| Hodinově     | Hodinově      |
| Stálý plat   | Stálý plat    |

### <a name="position-types"></a>Typy pozic 

Typy pozic používáte k popisu, zda je pozice na plný úvazek, částečný úvazek nebo jiná. Typy pozic jsou mapovány do Dayforce jako třídy mezd, které označují, zda zaměstnanec pracuje na plný nebo částečný úvazek.

Následující typy pozic a popisy jsou povinné.

| Typ pozice   | popis        |
|-----------------|--------------------|
| Plný úvazek       | Zaměstnanec na plný úvazek |
| Částečný úvazek       | Zaměstnanec na částečný úvazek |

### <a name="reason-codes"></a>Kódy důvodu

Kódy důvodů poskytují informace o stavu zaměstnance. Kódy důvodů jsou mapovány do Dayforce jako důvody stavů, které označují důvod pro změny stavu pozice nebo zaměstnání zaměstnance.

Následující kódy důvodů a popisy jsou povinné.

| Kód důvodu    | popis      | Použitelné scénáře |
|----------------|------------------|----------------------|
| RESIGNATION    | Výpověď      | Dát pracovníkovi výpověď     |
| TERMINATION    | Ukončení      | Dát pracovníkovi výpověď     |
| RETIREMENT     | Důchod       | Dát pracovníkovi výpověď     |
| JINÝ          | Jiné důvody    | Dát pracovníkovi výpověď     |
| DEATH          | Úmrtí            | Dát pracovníkovi výpověď     |
| LEAVEOFABSENCE | Dovolená | Dát pracovníkovi výpověď     |
| CONTRACTEND    | Konec smlouvy  | Dát pracovníkovi výpověď     |
| SALARYCHANGE   | Změna platu | Kompenzace         |

### <a name="marital-status"></a>Rodinný stav

Hodnoty rodinného stavu jsou mapovány do Dayforce a překládány podle potřeby na přijaté hodnoty při integraci.

Následující tabulka zobrazuje, jak jsou hodnoty rodinného stavu mapovány do Dayforce.

| Talent                 | Dayforce             |
|------------------------|----------------------|
| Ženatý/vdaná                | Ženatý/vdaná              |
| Jedno                 | Jedno               |
| Vdovec/vdova                | Vdovec/vdova              |
| Rozvedený/rozvedená               | Rozvedený/rozvedená             |
| Registrované partnerství | Domácí partnerství |
| None                   | None                 |
| Společná domácnost             | Společná domácnost           |

### <a name="gender"></a>Rod

Označení pohlaví jsou mapována do Dayforce a překládána podle potřeby na přijaté hodnoty při integraci.

Následující tabulka zobrazuje, jak jsou označení pohlaví mapována do Dayforce.

| Talent       | Dayforce        |
|--------------|-----------------|
| Muž         | Muž            |
| Žena       | Žena          |
| Nespecifické | *Nepodporováno* |

### <a name="earning-codes"></a>Kódy příjmů

Kódy příjmů jedinečným způsobem identifikují každý typ příjmu, který zaměstnanci dostávají. Kódy pokrývají několik parametrů, které souvisejí s příjmy, například účetní pravidla, daňové předpisy, požadavky na vykazování a funkci hrubé mzdy. Pokud použijete nepodporovaný interval, interval **Každá mzda** se použije jako výchozí pro výpočet.

#### <a name="supported-frequencies"></a>Podporované intervaly

- Všechna
- EVERYPAY
- EACHPAYPERIOD
- EVRYOTHRPAYODD
- EVRYOTHRPAYEVN
- 1OFMTH
- LASTOFMTH
- 2OFMTH
- 3OFMTH
- 4OFMTH
- 5OFMTH
- 1N2OFMTH
- 3N4OFMTH
- 1N3OFMTH
- 1N4OFMTH
- 2N3OFMTH
- 2N4OFMTH
- 1N2N3OFMTH
- 1N2N4OFMTH
- 1N3N4OFMTH
- 2N3N4OFMTH
- 1N2N3N4OFMTH - 1N2N3N4OFMTH
- 2N3N4N5OFMth - 2N3N4N5OFMth
- 1OFQTR - 1OFQTR
- LASTOFQTR – LASTOFQTR
- LASTMTHOFQTR – LASTMTHOFQTR
- 1OFYEAR - 1OFYEAR
- LASTOFYEAR – LASTOFYEAR
- NOVNDECOFYEAR - NOVNDECOFYEAR

### <a name="addresses"></a>Adresy

Identifikace konkrétních kódů země nebo oblasti, státu a okresu vyžaduje konkrétní formáty, které Dayforce a místní poskytovatelé mohou rozpoznat. Ačkoliv je formát pro města flexibilní, je nutné přiřadit ke každému městu stát.

| Talent          | Dayforce              |
|-----------------|-----------------------|
| Země nebo oblast  | Kód země          |
| PSČ | PSČ           |
| Kraj           | Kód státu            |
| Město            | Město                  |
| Okres          | Okres |
| Ulice          | Řádek adresy 1        |

### <a name="tax-regions"></a>Daňové oblasti

Oblasti daně se používají pro určení příslušné daně, která se má použít během generování mzdy. Daňové oblasti jsou mapovány na Dayforce jako adresy místa. Výchozí oblasti daně musí být přidruženy k aktivní pozici pracovníka. 

- Daňová oblast (povinná)
- Země/oblast (povinné)
- Stát (povinný)
- Okres 
- Město (povinné)

## <a name="configure-your-data-to-generate-payroll-in-mexico"></a>Konfigurace dat pro generování mezd v Mexiku

Když generujete mzdu pro zaměstnance v Mexiku, musí být nakonfigurovány následující prvky:

- Pro pozice jsou požadována oddělení.
- Nákladová střediska musí být nastavena jako finanční dimenze a musí být prvním prvkem ve výchozím řetězci finanční dimenze.

### <a name="job-types"></a>Typ úloh

Typy prací se používají pro seskupení podobných pozic do kategorií. Typy práce jsou povinné pro zpracování mezd v Mexiku. Příklady typů prací zahrnují plný úvazek a částečný úvazek, nebo plat a hodinovou mzdu. Typy prací jsou mapovány do Dayforce jako typy mezd, které označují, zda je zaměstnanec vyplácen hodinově nebo mzdou.

Následující typy práce a popisy jsou povinné.

| Typ práce   | popis |
|------------|-------------|
| Hodinově     | MX hodinově   |
| Stálý plat   | MX Stálý plat |

### <a name="position-types"></a>Typy pozic 

Typy pozic používáte k popisu, zda je pozice na plný úvazek, částečný úvazek nebo jiná. Typy pozic jsou mapovány do Dayforce jako třídy mezd, které označují, zda zaměstnanec pracuje na plný nebo částečný úvazek.

Následující typy pozic a popisy jsou povinné.

| Typ pozice   | popis        |
|-----------------|--------------------|
| Plný úvazek       | Zaměstnanec na plný úvazek |
| Částečný úvazek       | Zaměstnanec na částečný úvazek |

### <a name="reason-codes"></a>Kódy důvodu

Kódy důvodů poskytují informace o stavu zaměstnance. Kódy důvodů jsou mapovány do Dayforce jako důvody stavů, které označují důvod pro změny stavu pozice nebo zaměstnání zaměstnance.

Následující kódy důvodů a popisy jsou povinné.

| Kód důvodu            | popis                    | Použitelné scénáře |
|------------------------|--------------------------------|----------------------|
| DEPARTUREBEFOREPAYMENT | Odchod před první mzdou | Dát pracovníkovi výpověď     |
| RESIGNATION            | Výpověď                    | Dát pracovníkovi výpověď     |
| PENSION                | Důchod                        | Dát pracovníkovi výpověď     |
| TERMINATION            | Ukončení                    | Dát pracovníkovi výpověď     |
| RETIREMENT             | Důchod                     | Dát pracovníkovi výpověď     |
| ABSENTEE               | Nepřítomný                       | Dát pracovníkovi výpověď     |
| JINÝ                  | Jiné důvody                  | Dát pracovníkovi výpověď     |
| CLOSURE                | Obchodní uzávěrka               | Dát pracovníkovi výpověď     |
| DEATH                  | Úmrtí                          | Dát pracovníkovi výpověď     |
| LEAVEOFABSENCE         | Dovolená               | Dát pracovníkovi výpověď     |
| CONTRACTEND            | Konec smlouvy                | Dát pracovníkovi výpověď     |
| SALARYCHANGE           | Změna platu               | Kompenzace         |

### <a name="terms-of-employment"></a>Podmínky zaměstnání

Podmínky zaměstnání se použijí k vytvoření kategorií podmínek zaměstnání. Podmínky jsou mapovány na Dayforce jako hodnoty indikátoru zaměstnání.

Následující podmínky zaměstnání a popisy jsou povinné.

| Podmínky zaměstnání   | popis |
|-----------------------|-------------|
| Řádné               | Řádné     |
| Přímo                | Přímo      |
| Stáž            | Stáž  |
| Trvalé             | Trvalé   |

### <a name="marital-status"></a>Rodinný stav

Hodnoty rodinného stavu jsou mapovány do Dayforce a překládány podle potřeby na přijaté hodnoty při integraci.

Následující tabulka zobrazuje, jak jsou hodnoty rodinného stavu mapovány do Dayforce.

| Talent                 | Dayforce                  |
|------------------------|---------------------------|
| Ženatý/vdaná                | Ženatý/vdaná                   |
| Jedno                 | Jedno                    |
| Vdovec/vdova                | Vdovec/vdova                   |
| Rozvedený/rozvedená               | Rozvedený/rozvedená                  |
| Registrované partnerství | Domácí partnerství      |
| None                   | *Nepodporováno v Mexiku* |
| Společná domácnost             | *Nepodporováno v Mexiku* |

### <a name="gender"></a>Rod

Označení pohlaví jsou mapována do Dayforce a překládána podle potřeby na přijaté hodnoty při integraci.

Následující tabulka zobrazuje, jak jsou označení pohlaví mapována do Dayforce.

| Talent       | Dayforce                  |
|--------------|---------------------------|
| Muž         | Muž                      |
| Žena       | Žena                    |
| Nespecifické | *Nepodporováno v Mexiku* |

### <a name="payment-method"></a>Způsob platby

Způsoby platby poskytuje zaměstnanci a společnosti způsob, jak bude vyplácen zaměstnanec. Metody platby jsou mapovány do Dayforce a překládány podle potřeby na přijaté hodnoty při integraci.

Následující tabulka zobrazuje, jak jsou metody platby mapována do Dayforce.

| Talent             | Dayforce                  |
|--------------------|---------------------------|
| Hotovost               | Hotovost                      |
| Elektronická platba | Převod                  |
| Kontrola              | Šek                    |
| Bankovní směnka         | *Nepodporováno v Mexiku* |
| Další              | *Nepodporováno v Mexiku* |

### <a name="bank-account-type"></a>Typ bankovního účtu

Typy bankovního účtu se používají pro elektronické platby zaměstnancům. Typy bankovního účtu jsou mapovány do Dayforce jako informace o převodním účtu. Typy bankovního účtu jsou překládány podle potřeby na přijaté hodnoty při integraci.

| Talent            | Dayforce                  |
|-------------------|---------------------------|
| Běžný účet  | CheckingAccount           |
| Mzdový účet   | PayrollAccount            |
| Spořicí účet   | *Nepodporováno v Mexiku* |
| BankGirot účet | *Nepodporováno v Mexiku* |
| PlusGirot účet | *Nepodporováno v Mexiku* |

### <a name="earning-codes"></a>Kódy příjmů

Kódy příjmů jedinečným způsobem identifikují každý typ příjmu, který zaměstnanci dostávají. Kódy pokrývají několik parametrů, které souvisejí s příjmy, například účetní pravidla, daňové předpisy, požadavky na vykazování a funkci hrubé mzdy. Pokud použijete nepodporovaný interval, interval **Každá mzda** se použije jako výchozí pro výpočet.

#### <a name="supported-frequencies"></a>Podporované intervaly

- Všechna
- EVERYPAY
- EACHPAYPERIOD
- EVRYOTHRPAYODD
- EVRYOTHRPAYEVN
- 1OFMTH
- LASTOFMTH
- 2OFMTH
- 3OFMTH
- 4OFMTH
- 5OFMTH
- 1N2OFMTH
- 3N4OFMTH
- 1N3OFMTH
- 1N4OFMTH
- 2N3OFMTH
- 2N4OFMTH
- 1N2N3OFMTH
- 1N2N4OFMTH
- 1N3N4OFMTH
- 2N3N4OFMTH
- 1N2N3N4OFMTH - 1N2N3N4OFMTH
- 2N3N4N5OFMth - 2N3N4N5OFMth
- 1OFQTR - 1OFQTR
- LASTOFQTR – LASTOFQTR
- LASTMTHOFQTR – LASTMTHOFQTR
- 1OFYEAR - 1OFYEAR
- LASTOFYEAR – LASTOFYEAR
- NOVNDECOFYEAR - NOVNDECOFYEAR

### <a name="addresses"></a>Adresy

Identifikace konkrétních kódů země nebo oblasti, státu a okresu vyžaduje konkrétní formáty, které Dayforce a místní poskytovatelé mohou rozpoznat. Ačkoliv je formát pro města flexibilní, je nutné přiřadit ke každému městu stát.

| Talent              | Dayforce              |
|---------------------|-----------------------|
| Země nebo oblast      | Kód země          |
| PSČ     | PSČ           |
| Kraj               | Kód státu            |
| Město                | Město                  |
| Okres              | Okres |
| Ulice              | Řádek adresy 1        |
| Číslo popisné       | Řádek adresy 2        |
| Doplňující název budovy | Řádek adresy 5        |

### <a name="passport-number"></a>Číslo cestovního pasu

Zaměstnanci mohou deklarovat informace o cestovním pasu. Tato informace je typu identifikace **Pas** a je integrována do Dayforce jako součást informací o zaměstnanci specifických pro Mexiko.

- Typ identifikace = Pas
- Datum vydání
- Datum vypršení platnosti

Zaměstnanec může deklarovat více identifikačních čísel typu identifikace **Pas**. Do aplikace Dayforce se integruje pouze zadání aktuálního aktivního pasu. Po uplynutí platnosti všech zadání pasu se integruje do Dayforce ten, který byl naposledy vydán.
