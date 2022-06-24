---
title: Obchody správy rabatu
description: Tento článek popisuje, jak vytvořit nabídky správy rabatu. Nabídky se používají k řízení různých metod a základů pro výpočet rabatů a autorských poplatků. Zahrnují pravidla pro zahrnutí a vyloučení.
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TAMRebateDeal
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 28cfff69ab4e528c146ccbf6a34548a819c99522
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8851587"
---
# <a name="rebate-management-deals"></a>Nabídky správy rabatu

[!include [banner](../includes/banner.md)]

Nabídky správy rabatu se používají k řízení různých metod a základů pro výpočet rabatů a autorských poplatků. Zahrnují pravidla pro zahrnutí a vyloučení. Existují tři typy nabídek správy rabatů: rabaty zákazníků, autorské poplatky zákazníků a rabaty dodavatelů. Všechny tři typy používají podobná nastavení. Tento článek poukazuje na rozdíly tam, kde existují.

## <a name="create-a-deal"></a>Vytvoření nabídky

1. Přejděte na **Správa rabatu \> Nabídky správy rabatu \> Všechny nabídky správy rabatu**. Na stránce se seznamem **Všechny nabídky správy rabatu** můžete vytvářet a pracovat s nabídkami všech tří typů.

    Popřípadě proveďte jeden z následujících kroků. V každém případě stránka se seznamem, která se zobrazí, poskytuje všechna stejná nastavení jako stránka se seznamem **Všechny nabídky správy rabatu**, ale je filtrována, aby zobrazovala nabídky pouze jednoho typu.

    - Přejděte na **Správa rabatu \> Nabídky správy rabatu \> Nabídky rabatu zákazníků** a vytvářejte pouze nabídky rabatu zákazníků.
    - Přejděte na **Správa rabatu \> Nabídky správy rabatu \> Nabídky autorských poplatků zákazníků** a vytvářejte pouze nabídky autorských poplatků zákazníků.
    - Přejděte na **Správa rabatu \> Nabídky správy rabatu \> Nabídky rabatu dodavatele** a vytvářejte pouze nabídky rabatu dodavatele.

1. V podokně akcí zvolte **Nový**.
1. V dialogovém okně **Vytvořit novou nabídku** nastavte následující pole:

    - **Nabídka správy poplatku** - Pokud jste [nastavili číselnou řadu](rebate-management-parameters.md) pro nabídky rabatu, je toto pole automaticky nastaveno na jedinečné, systémem vygenerované ID. V opačném případě zadejte jedinečné ID.
    - **Popis** - Zadejte popis nabídky.
    - **Modul** - Vyberte typ partnera, kterého se nabídky týká (*Zákazník* nebo *Dodavatel*). V závislosti na stránce, ze které jste začali, může být toto pole automaticky nastaveno na základě zvoleného typu nabídky. V tomto případě je pole pouze pro čtení.
    - **Typ** - Vyberte typ nabídky (*Rabat* nebo *Autorský poplatek*). V závislosti na stránce, ze které jste začali, může být toto pole automaticky nastaveno na základě zvoleného typu nabídky. V tomto případě je pole pouze pro čtení.
    - **Odsouhlasit podle** - Vyberte způsob výpočtu a odsouhlasení nabídky:

        - *Nabídky* - Pro všechny rabaty a odpočty v nabídce by měl být zpracován jeden rabat.
        - *Řádek* - Rabaty by měly být zpracovány pro každý řádek v nabídce.

    - **Účetní profil** - Vyberte [Účetní profil](rebate-management-posting.md), který použijete pro transakce, u nichž platí nabídka. Toto pole je dostupné pouze v případě, že pole **Odsouhlasit podle** je nastaveno na *Nabídka*. Pokud je nastaveno na *Řádek*, přiřadíte profil později pro každý řádek, který přidáte k nabídce.
    - **Účetní profil pro záruku** - Vyberte [Účetní profil](rebate-management-posting.md), který použijete pro transakce záruky. Profily účtování jsou vyžadovány pro transakce záruky pouze v případě, že se záruka vztahuje na autorský poplatek. Jinak, ačkoliv účetní profil není povinný, pokud není zadán žádný účetní profil, při účtování záruk se zobrazí chyba. Toto pole je dostupné pouze v případě, že pole **Typ** je nastaveno na *Autorský poplatek*. 
    - **Výstup rabatu** - Vyberte, jak má být zaplacen rabat nebo autorský poplatek:

        - *Finanční* - Vytvořte dobropis s volným textem nebo dluhopis závazků, aby bylo možné peníze vyplatit nebo přijmout později. Všimněte si, že dodávky **lze** použít s rabaty, kde je vybrána tato možnost. Tato možnost je jediná dostupná možnost v případě, že pole **Typ** je nastaveno na *Autorský poplatek*.
        - *Položka* - Vygenerujte prodejní objednávku pro položky podle nastavení nabídky. Na této prodejní objednávce je každé položce přiřazena cena 0 (nula). Všimněte si, že dodávky **nelze** použít s rabaty, kde je vybrána tato možnost.

    - **Měna rabatu** - Vyberte měnu, která se má použít při vyplácení rabatu, odpočtu nebo autorského poplatku.
    - **Poznámky k dokumentu** - Podle potřeby zadejte poznámky k nabídce.
    - **Kumulativní záruka** - Tuto možnost můžete nastavit na *Ano*, pouze pokud je pole **Typ** nastaveno na *Autorský poplatek*. Tato možnost ovlivňuje výpočet plateb zaručených odpočtů. Následuje příklad:

        - Zárukou nabídky je prodej hodnoty, která povede k platbě 10 000 USD za čtvrtletí.
        - Organizace, která prodává zboží, prodává v 1. čtvrtletí hodnotu, která způsobí odpočet ve výši 12 000 USD. Výsledkem je autorský poplatek 12 000 USD, který je zaplacen, minus záruka 10 000 USD.
        - Pokud je možnost **Kumulativní záruka** nastavena na *Ano*, další 2 000 USD autorských poplatků, které byly vyplaceny v 1. čtvrtletí, se vztahují na 2. čtvrtletí. Proto je zákazníkovi zaručeno 8 000 USD (záruka 10 000 USD minus dodatečná platba 2 000 USD).
        - Ve 2. čtvrtletí zaregistrujete prodej, který aktivuje autorské poplatky 5 000 USD.
        - Systém identifikuje platbu 3 000 USD (záruka 8 000 USD minus 5 000 USD zaplacených autorských poplatků).
        - Pokud je možnost **Kumulativní záruka** nastavena na *Ne*, celých 10 000 USD je zaručeno každé čtvrtletí. Tato záruka odpovídá navrhované platbě 5 000 USD ve 2. čtvrtletí (záruka 10 000 USD minus 5 000 USD zaplacených autorských poplatků).

1. Vyberte **OK** pro vytvoření nabídky a zavřete dialogové okno.

Tento postup vytvoří úroveň záhlaví nové nabídky. Dále přidáte řádky k nabídce.

## <a name="add-lines-to-a-deal"></a>Přidání řádků k nabídce

Jakmile vytvoříte nabídku, jak je popsáno v předchozí části, můžete ji otevřít na stránce se seznamem. Poté můžete přidat řádky k identifikaci zákazníků nebo dodavatelů, položek, časových rámců, základu a metod výpočtu pro nabídku. Nabídka může mít jeden nebo více řádků. Pokud má nabídka více řádků, jsou obecně stejného typu, nebo jsou k nim přidruženy stejné parametry. Dokud k nabídce nepřidáte řádky, nabídka ve skutečnosti nic neudělá.

1. Otevřete příslušnou stránku se seznamem nabídek rabatu, jak je popsáno v předchozí části.
1. Najděte a otevřete nabídku, se kterou chcete pracovat.
1. Na záložce s náhledem **Správa rabatu** vyberte jedno z následujících tlačítek a přidejte řádek nabídky do mřížky:

    - **Přidat řádek** - Přidejte nový, prázdný řádek nabídky.
    - **Kopírovat řádek** - Pokud se stávající řádek nabídky podobá řádku nabídky, kterou chcete přidat, můžete toto tlačítko zkopírovat a přidat jeho kopii. Nový řádek nabídky bude obsahovat všechna nastavení ze souvisejících podrobností správy rabatu. Poté můžete upravit nastavení. Například obvykle aktualizujete vztah položky a procento rabatu.

1. Na novém řádku nabídky nastavte následující pole:

    - **Číslo správy poplatku** - Pokud jste [nastavili číselnou řadu](rebate-management-parameters.md) pro čísla správy rabatu, je toto pole automaticky nastaveno na jedinečné, systémem vygenerované ID. V opačném případě zadejte jedinečné ID.
    - **Typ** - Typ nabídky, na kterou se řádka vztahuje (*Rabat* nebo *Autorský poplatek*). Hodnota je zkopírována ze záhlaví a nelze ji změnit.
    - **Popis** - Zadejte popis řádku nabídky.
    - **Společnost** - Vyberte společnost (právnickou osobu), na kterou se vztahuje řádek nabídky. Během zpracování mohou uživatelé zpracovávat pouze řádky nabídky, které jsou přiřazeny společnosti, kterou aktuálně používají. Stránka se seznamem **Nabídky rabatů zákazníka** poskytuje zobrazení více společností na základě zabezpečeného přístupu uživatele. Rabaty však můžete upravovat a zpracovávat pouze pro společnost, kterou právě používáte.
    - **Kód obchodního vztahu** - Vyberte rozsah zákazníků nebo dodavatelů, na které se vztahuje řádek nabídky:

        - *Tabulka* - Řádek nabídky se vztahuje na konkrétního zákazníka nebo dodavatele.
        - *Skupina* - Řádek nabídky se vztahuje na skupinu zákazníků nebo dodavatelů. Další informace o nastavení skupin naleznete v části [Skupiny správy rabatu](rebate-management-groups.md).
        - *Vše* - Řádek nabídky se vztahuje na všechny zákazníky nebo dodavatele.

    - **Vztah obchodního vztahu** – Pokud jste vybrali *Tabulka* v poli **Kód obchodního vztahu**, vyberte zákazníka nebo dodavatele, kterého se nabídka týká. Pokud jste vybrali možnost *Skupina*, vyberte skupinu zákazníka nebo dodavatele. Pokud jste vybrali možnost *Vše*, toto pole není dostupné.
    - **Kód položky** - Vyberte rozsah položek, na které se vztahuje řádek nabídky:

        - *Tabulka* - Řádek nabídky se vztahuje na konkrétní položku.
        - *Skupina* - Řádek nabídky se vztahuje na skupinu položek. Další informace o nastavení skupin naleznete v části [Skupiny správy rabatu](rebate-management-groups.md).
        - *Vše* – Řádek nabídky platí pro všechny položky.

    - **Vztah položky** – Pokud jste vybrali *Tabulka* v poli **Kód položky**, vyberte položku, kterého se řádek nabídky týká. Pokud jste vybrali možnost *Skupina*, vyberte skupinu položek. Pokud jste vybrali možnost *Vše*, toto pole není dostupné.
    - **Typ jednotky** – Vyberte typ jednotky, který se vztahuje na řádek nabídky (*Skladová jednotka* nebo *Jednotka skutečné hmotnosti*). U starších záznamů může být toto pole prázdné. V tomto případě se předpokládá hodnota *Skladová jednotka*.
    - **(Parametry správy zásob)** - Ve zbývajících polích na řádku nabídky zadejte hodnoty parametrů správy zásob, které se použijí k definování položek zahrnutých do nabídky (například velikost položky, barva, styl, pracoviště a sklad). Chcete-li přidat nebo odebrat dimenze, vyberte **Zobrazit dimenze** v podokně akcí.

1. V podokně akcí vyberte **Uložit**.
1. Chcete-li dále omezit sadu položek, na které se vztahuje řádek nabídky, vyberte řádek a poté na záložce s náhledem **Správa rabatu** vyberte **Filtr** a otevřete standardní dialogové okno **Dotaz**.
1. Pro každý řádek nabídky, který přidáte, nastavte podrobnosti výpočtu a další podrobnosti na záložce s náhledem **Podrobnosti správy rabatu**, jak je popsáno v další části.

## <a name="add-rebate-management-details-to-a-deal-line"></a>Přidání podrobností správy rabatu na řádek nabídky

Pro každý řádek vaší nabídky musíte nastavit podrobnosti na záložce s náhledem **Podrobnosti správy rabatu**. Nejprve vyberte řádek nabídky na záložce s náhledem **Správa rabatu**. Poté nastavte hodnoty pro tento řádek nabídky pomocí různých karet na záložce s náhledem **Podrobnosti správy rabatu**. Následující pododdíly popisují, jak používat jednotlivé karty.

### <a name="settings-on-the-general-tab"></a>Nastavení na kartě Obecné

Karta **Obecné** na záložce s náhledem **Podrobnosti správy rabatu** umožňuje nastavit metodu a základ výpočtu pro vybraný řádek nabídky. Toto nastavení řídí, zda je vyžadován minimální nákup, účetní profily, které jsou přidruženy k řádku nabídky obchodu, a podrobnosti výpočtu. V následující tabulce jsou popsána pole, která jsou k dispozici.

| Pole | popis |
|---|---|
| Metoda výpočtu | Vyberte metodu, která se použije, když je vybraný řádek nabídky kombinován s jinými řádky nabídky (*Kroková*, *Kumulativní*, *Postupná* nebo *Celková*). Hodnota tohoto pole může dramaticky ovlivnit výsledek vašich výpočtů rabatu. Úplný popis každé metody a příklady, které ukazují, jak ovlivňuje výpočet rabatu, najdete v části [Metody výpočtu pro řádky nabídky](#calc-methods) dále v tomto článku. |
| Základ | Vyberte, zda se rabat použije na základě množství (tedy celkového počtu zakoupených nebo prodaných jednotek) nebo hodnoty (tedy celkové ceny zakoupeného nebo prodaného zboží). |
| Typ transakce | <p>Vyberte bod v procesu, kdy má dojít k výpočtu:</p><ul><li>*Objednávka* - Jako základ pro výpočet použijte objednané množství nebo hodnotu.</li><li>*Doručeno* - Jako základ pro výpočet použijte doručené množství nebo hodnotu.</li><li>*Faktura* - Jako základ pro výpočet použijte vyfakturované množství nebo hodnotu.</li></ul> |
| Jednotka | Pokud jste vybrali *Množství* v poli **Základ**, vyberte jednotku, ve které musí být uvedeno množství. |
| Minimální částka | Zadejte minimální částku, která musí být zaplacena za období. Můžete zadat zápornou hodnotu, abyste povolili záporné částky rabatu, pokud dobropisy překročí prodej za dané období. |
| Zásady snižování rabatu | Vyberte [zásady snižování rabatu](rebate-reduction-principle.md), které se vztahují na řádek nabídky. |
| Číslo varianty | Pokud se řádek nabídky vztahuje na položku, která má varianty, vyberte variantu, na kterou se řádek nabídky vztahuje. |
| Základ rabatu dodavatele | <p>Toto pole se zobrazuje pouze pro rabaty dodavatele (to znamená nabídky, kde pole **Modul** je nastaveno na *Dodavatel*). Vyberte základ pro rabat dodavatele:</p><ul><li>*Nákupní objednávka* - Rabat, který prodejce obdrží, je založen na množství nebo hodnotě na nákupní objednávce.</li><li>*Prodejní objednávka* - Dodavatel obdrží rabat až po prodeji zboží. Rabat je založen na množství nebo hodnotě na prodejní objednávce.</li></ul> |
| Základ ceny | <p>Toto pole se zobrazuje pouze pro rabaty dodavatele (nabídky, kde pole **Modul** je nastaveno na *Dodavatel*). Pokud jste vybrali *Prodejní objednávka* v poli **Základ rabatu dodavatele**, vyberte příslušný základ ceny:</p><ul><li><p>*FIFO* - Periodická úloha **Vypočítat nákupní cenu FIFO** pro výpočet rabatu musí být spuštěna. (Chcete-li úlohu spustit, přejděte na **Správa rabatu \> Pravidelné úkoly \> Vypočítat nákupní cenu FIFO**.) K výpočtu hodnoty prodávaného skladu se použije pravidlo FIFO. Tato hodnota se poté použije k výpočtu rabatů dodavatele. Následuje příklad:</p><ul><li>**Prodaný sklad.** 1 000 jednotek po 3 USD = 3 000 USD</li><li>**Aktuální nákupní cena na základě FIFO:** 2 USD</li><li>**Pracovní výpočet:** *Prodané jednotky* × *Aktuální nákupní cena* = 1 000 × 2 USD = 2 000 USD</li></ul></li><li><p>*Poslední nákupní cena* - Hodnota z poslední nákupní transakce bude použita k výpočtu rabatů dodavatele. Následuje příklad:</p><ul><li>**Prodaný sklad.** 1 000 jednotek po 3 USD = 3 000 USD</li><li>**Poslední nákupní cena:** 2 USD</li><li>**Pracovní výpočet:** *Prodané jednotky* × *Poslední nákupní cena* = 1 000 × 2 USD = 2 000 USD</li></ul></li><li><p>*Průměrná nákupní cena* - Vážená průměrná hodnota za posledních *X* měsíců bude použity k výpočtu rabatů dodavatele. Pokud vyberete tuto možnost, musíte do pole **Počet měsíců** zadat počet měsíců (které je k dispozici pouze v případě, že pole **Základ ceny** je nastaveno na *Průměrná nákupní cena*). Následuje příklad:</p><ul><li>**Prodaný sklad.** 1 000 jednotek po 3 USD = 3 000 USD</li><li>**Průměrná nákupní cena:** 2 USD</li><li>**Pracovní výpočet:** *Prodané jednotky* × *Průměrná nákupní cena* = 1 000 × 2 USD = 2 000 USD</li></ul></li><li><p>*Prodejní cena* - Prodejní cena bude použita k výpočtu rabatů dodavatele. Následuje příklad:</p><ul><li>**Prodaný sklad.** 1 000 jednotek po 3 USD = 3 000 USD</li><li>**Průměrná nákupní cena:** 2 USD</li><li>**Pracovní výpočet:** *Prodané jednotky* × *Prodejní cena* = 1 000 × 3 USD = 3 000 USD</li></ul></li></ul> |
| Počet měsíců | Toto pole se zobrazuje pouze pro rabaty dodavatele (nabídky, kde pole **Modul** je nastaveno na *Dodavatel*). Pokud jste vybrali *Průměrná kupní cena* v poli **Základ ceny** zadejte počet měsíců, který má být použit. |
| Účetní profil | Zvolte [účetní profil](rebate-management-posting.md), který se vztahuje na zvolený řádek nabídky. Tento profil se používá pouze v případě, že pole **Odsouhlasit podle** v záhlaví nabídky je nastaveno na *Řádek*. Pokud je pole **Odsouhlasit podle** nastaveno na *Nabídka*, vždy se použije účetní profil, který je nastaven v záhlaví nabídky. Pokud na řádku nabídky není nastaven žádný účetní profil, použije se účetní profil, který je nastaven v záhlaví nabídky. |
| Účetní profil pro záruku | Toto pole funguje jako pole **Účetní profil**, ale vztahuje se pouze na autorské poplatky. |
| Typ platby | Typ platby pro účetní profil, který je vybrán pro nabídku. |
| Včetně DPH | Vyberte, zda transakce zahrnuje daň. Zahrnutí daně je relevantní pouze tehdy, když je pole **Základ** nastaveno na *Hodnota*. Částka na faktuře bude použita jako částka včetně daně. Pokud je výpočet rabatu založen na procentu, systém vynásobí procento rabatu částkou včetně daně. Všimněte si, že výpočet používá hodnotu DPH z řádku nabídky. |
| Zahrnout dobropisy | <p>Tuto možnost nastavte na *Ano*, chcete-li zahrnout dobropisy do výpočtu rabatu.</p><p>Pokud nastavíte tuto možnost na *Ano*, účinek se liší v závislosti na hodnotě pole **Typ transakce**:</p><ul><li>Pokud je pole **Typ transakce** nastaveno na *Faktura*, bude výpočet zohledňovat dobropisy. Tato konfigurace je obvyklá konfigurace.</li><li>Pokud je pole **Typ transakce** nastaveno na *Objednávka*, bude výpočet zohledňovat prodejní objednávky, které mají záporné hodnoty, i otevřené vratky.</li></ul> |
| Částka slevy | Tuto možnost nastavte na *Ano* pro založení výpočtu na zlevněné částce položky nebo položek v případech, kdy jsou uvedeny slevy na řádku nabídky. |
| Pouze zaplacené faktury | Tuto možnost nastavte na *Ano*, pokud by výpočet měl zohledňovat pouze plně zaplacené faktury. (Jinými slovy, rabaty se nebudou počítat u částečně zaplacených faktur.) Tato možnost je k dispozici, pouze když je pole **Typ transakce** nastaveno na *Faktura*. |
| Zahrnout volný text | Tuto možnost nastavte na *Ano*, chcete-li zahrnout do výpočtu volnou fakturu. Volné faktury lze zahrnout pouze pro řádky nabídky, kde je pole **Kód položky** nastaveno na *Vše*. |
| Zahrnout slevu pro vyrovnání | Tuto možnost nastavte na *Ano*, chcete-li snížit rabat o první slevu pro vyrovnání. Předpokládá se, že organizace přijme první slevu pro vyrovnání. Tuto možnost nastavte na *Ne*, chcete-li umožnit pozdější použití slevy pro vyrovnání. |
| Poznámky k dokumentu | Zadejte poznámky, které by se měly použít jako text transakce na řádcích deníku transakcí rabatů. |

### <a name="settings-on-the-dates-tab"></a>Nastavení na kartě Data

Nastavení na kartě **Data** na záložce s náhledem **Podrobnosti správy rabatu** definuje frekvenci a načasování výpočtů, které jsou určeny na kartě **Obecné**. Určuje, jak dochází k výpočtům v době zpracování.

Tato karta umožňuje určit rozsah dat, pro který je vybraný řádek nabídky platný, a frekvenci výpočtu. Můžete také určit, zda a kdy má být zaúčtována záruka.

Tlačítka na panelu nástrojů můžete používat k přidání řádků dat do mřížky nebo jejich odstranění. Pokud existuje více řádků data, nesmí se platná období překrývat. V opačném případě se při pokusu o uložení nabídky zobrazí chybová zpráva.

V následující tabulce jsou popsána pole, která jsou k dispozici pro každý řádek data.

| Pole | popis |
|---|---|
| Od data | Zadejte první datum, kterého se řádek data týká. Pokud jsou v záhlaví nabídky zadána data „od“ a „do“, použijí se jako výchozí hodnoty pro každý nový řádek data. |
| Do data | Zadejte poslední datum, kterého se řádek data týká. Pokud jsou v záhlaví nabídky zadána data „od“ a „do“, použijí se jako výchozí hodnoty pro každý nový řádek data. |
| Za | Určete, jak často by se měl počítat řádek nabídky. Zde zadejte celé číslo a poté vyberte jednotku v poli **Kumulovat za**. Chcete-li například vypočítat každý druhý týden, nastavte pole **Za** na *2* a pole **Kumulovat za** na *Týdny*. |
| Kumulovat za | Vyberte jednotku, která se vztahuje na nastavení **Za**. Vyberte *Životnost* pro vypočet po celou dobu životnosti řádku nabídky. Vyberte *Přizpůsobené období* a zvolte období, které je definováno v hlavní knize. V tomto případě musíte také nastavit pole **Typ období**. |
| Typ období | Toto pole je dostupné pouze v případě, že pole **Kumulovat za** je nastaveno na *Přizpůsobené období*. Hodnoty, které jsou k dispozici pro výběr, pocházejí z typů období, které jsou definovány v hlavní knize. |
| První den v týdnu | Určete, jak jsou týdny identifikovány pro dané období. Toto pole je dostupné pouze v případě, že pole **Kumulovat za** je nastaveno na *Týdny*. |
| Nárokovat za | Uveďte, jak často je možné nárokovat peníze rabatu za řádek nabídky. Zde zadejte celé číslo a poté vyberte jednotku v poli **Nárokovat za**. |
| Nárokovat podle | Vyberte jednotku, která se vztahuje na nastavení **Nárokovat za**. Vyberte *Životnost* pro povolení nároků pouze jednou během celé životnosti řádku nabídky. Vyberte *Přizpůsobené období* a zvolte období, které je definováno v hlavní knize. V tomto případě musíte také nastavit pole **Typ období nároku**. |
| Typ období nároku | Toto pole je dostupné pouze v případě, že pole **Nárokovat podle** je nastaveno na *Přizpůsobené období*. Hodnoty, které jsou k dispozici pro výběr, pocházejí z typů období, které jsou definovány v hlavní knize. |
| Zpracování při zaúčtování | Toto políčko zaškrtněte, pokud má být řádek nároku zpracován v době zaúčtování. Tato možnost je k dispozici pouze pro řádky nabídky, kde je pole **Typ transakce** na kartě **Obecné** nastavena na *Doručeno* nebo *Faktura*. U dodávek bude dodávka zaúčtována při vygenerování poznámky k dodání nebo faktury. |
| Záruka za | Toto pole se vztahuje pouze na nabídky autorských poplatků. Uveďte, jak často má být záruka autorského poplatku vypočítána během období, které je definováno nastavení **Kumulovat za**. Zde zadejte celé číslo a poté vyberte čas platby v poli **Záruka zaplacena**. |
| Záruka zaplacena | <p>Toto pole se vztahuje pouze na nabídky autorských poplatků. Funguje ve spojení s pole **Záruka za** pro definování frekvence výpočtu záruky. Vyberte jednu z následujících hodnot:</p><ul><li><p>*Začátek období* - Záruka se platí na začátku smluvního období, které je definováno pro řádek data. Nejprve je zpracována plná záruka. Jako autorský poplatek se zaúčtuje pouze hodnota autorských poplatků, která přesahuje zaručenou částku. Následuje příklad:</p><ul><li>**Záruka minimálně:** 10 000 USD po dobu dvou měsíců</li><li>**Měsíc 1:** 10 000 USD bylo zaúčtováno jako záruka a v autorských poplatcích byla zaúčtována 0</li><li>**Měsíc 2:** 2 000 USD bylo zaúčtováno do autorských poplatků a v zárukách byla zaúčtována 0</li><li>**Pracovní výpočet:** *Zbývající záruka* - *Zaúčtované autorské poplatky* = 0 USD- 2 000 USD = 2 000 USD.</li></ul><p>Protože je vyžadována platba autorských poplatků ve výši 2 000 USD, je pro 2 000 USD vytvořen deník.</p><p>**Poznámka:** Záruka by měla být vypočítána a zaúčtována společně s dodávkou odpočtů za první období.</p></li><li><p>*Konec období* - Záruka se nevyplácí až do konce smlouvy o odpočtech, jak je uvedeno v řádku data. Následuje příklad:</p><ul><li>**Záruka minimálně:** 10 000 USD po dobu dvou měsíců</li><li>**Měsíc 1:** 5 000 USD bylo zaúčtováno jako autorský poplatek a byl vytvořen deník.</li><li>**Měsíc 2:** 7 000 USD bylo zaúčtováno jako autorský poplatek a byl vytvořen deník.</li><li>**Pracovní výpočet:** Protože autorské poplatky přesahují částku záruky, zaúčtuje se do záruky 0 USD.</li></ul><p>**Poznámka:** Záruka by měla být vypočítána a zaúčtována pouze společně s transakcemi odpočtů a rabatů za konečné období.</p></li></ul> |
| Záruka minimálně | Toto pole se vztahuje pouze na nabídky autorských poplatků. Zadejte minimální částku záruky pro autorský poplatek v měně definované v záhlaví nabídky. |

### <a name="settings-on-the-lines-tab"></a>Nastavení na kartě Řádky

Karta **Řádky** na záložce s náhledem **Podrobnosti správy rabatu** umožňuje definovat řádky výpočtu pro vybraný řádek nabídky. Každý řádek výpočtu stanoví prahovou hodnotu pro množství nebo hodnotu a související částku nebo položky kompenzace. Pole **Základ** v možnosti **Obecné** určuje, zda je každý řádek výpočtu založen na množství nebo hodnotě.

Tlačítka na panelu nástrojů můžete používat k přidání řádků výpočtu do mřížky nebo jejich odstranění. Můžete mít libovolný počet řádků výpočtu. Pokud však existuje více řádků výpočtu, nesmí se rozsahy „do“ a „od“ množství nebo hodnot překrývat.

V následující tabulce jsou popsána pole, která jsou k dispozici pro každý řádek výpočtu.

| Pole | popis |
|---|---|
| Od množství/hodnoty | Zadejte minimální množství nebo hodnotu, na kterou se vztahuje řádek výpočtu. |
| Do množství/hodnoty | Zadejte maximální množství nebo hodnotu, na kterou se vztahuje řádek výpočtu. |
| Metoda správy rabatu | <p>Toto pole je k dispozici pouze pro nabídky, kde pole **Výstup rabatu** v záhlaví je nastaveno na *Finanční*. Vyberte způsob výpočtu rabatu.</p><ul><li>*Pevná* - Pro řádek se používá pevná částka ceny.</li><li>*Procento* - Použije se procento částky prodeje.</li><li>*Sazba* - Je použita pevná částka ceny za objednávku.</li></ul><p>**Důležité:** Důrazně doporučujeme použít stejnou metodu pro každý řádek výpočtu na kartě **Řádky**. Pokud je vyžadována nová metoda, vytvořte nový řádek nabídky. Pamatujte, že můžete použít tlačítko **Kopírovat řádek** na záložce s náhledem **Správa rabatu** k vytvoření nového řádku nabídky ze stávajícího řádku nabídky.</p><p>**Poznámka:** Pokud je pole **Výstup rabatu** nastaveno na *Položka*, toto pole je vždy nastaveno na *Pevná*. Další informace o tom, jak určit položky, najdete v textu, který následuje po této tabulce. |
| Částka správy rabatu | Toto pole je k dispozici pouze pro nabídky, kde pole **Výstup rabatu** v záhlaví je nastaveno na *Finanční*. Zadejte částku, která by měla být použita k výpočtu rabatu, na základě metody, kterou jste vybrali v poli **Metoda správy rabatu**. |

Jak bylo uvedeno v předchozí tabulce, u nabídek, kde je pole **Výstup rabatu** nastaveno na *Položka*, musíte určit položky, které budou poskytnuty pro každý řádek výpočtu na kartě **Řádky**. Chcete-li určit položky, postupujte takto.

1. Na kartě **Řádky** vytvořte požadovaný řádek výpočtu, pokud neexistuje, a vyberte ho.
1. Pokud nabídka nebyla uložena od vytvoření řádku výpočtu, vyberte **Uložit** v podokně akcí.
1. Na kartě **Řádky** vyberte **Položky**.
1. Na stránce **Položky** pomocí tlačítek v podokně akcí přidejte položky do mřížky nebo je podle potřeby odeberte. Pro každý řádek je třeba nastavit tato pole:

    - **Číslo položky** - Vyberte položku, která bude zadána.
    - **(Jiné dimenze)** - Pokud musíte k definování položky použít více dimenzí (například konfiguraci položky, velikost, barvu, styl, pracoviště nebo sklad), zadejte je. Chcete-li přidat nebo odebrat dostupné dimenze, vyberte **Zobrazit dimenze** v podokně akcí.
    - **Množství** - Zadejte množství, které bude poskytnuto po dosažení prahové hodnoty pro vybraný řádek výpočtu.
    - **Jednotka** - Vyberte jednotku, ve které je uvedena hodnota **Množství**.
    - **Násobek** – Toto pole se používá v kombinaci s polem **Množství**. Například na řádku položky nastavíte pole **Množství** na *2* a **Násobek** pole na *100*. Pokud pak máte celkové množství prodejní objednávky 150, dvě z položek budou zdarma (dvě za 100).

### <a name="settings-on-the-inventory-dimensions-tab"></a>Nastavení na kartě dimenze zásob

Karta **Dimenze zásob** na záložce s náhledem **Podrobnosti správy rabatu** zobrazuje všechny dostupné hodnoty dimenzí pro produkt, který je zadán pro vybraný řádek nabídky. Zahrnuje dimenze, které se nezobrazují na záložce s náhledem **Správa rabatu**. Hodnoty můžete upravit pouze pro ty dimenze, které se vztahují na vybraný produkt.

Můžete přidat další dimenze do mřížky na záložce s náhledem **Správa rabatu** výběrem možnosti **Zobrazit dimenze** v podokně akcí.

## <a name="calculation-methods-for-deal-lines"></a><a name="calc-methods"></a>Metody výpočtu pro řádky nabídky

Pokaždé, když nastavíte podrobnosti pro jeden ze svých řádků nabídky, jak je popsáno v předchozí části, musíte vybrat metodu výpočtu pro tento řádek. Tato část vysvětluje každou metodu výpočtu a poskytuje příklady, které ukazují, jak každá metoda vypočítává celkový rabatu za objednávky a řádky nabídek. V těchto příkladech jsou objednávky a řádky nabídek identické. Liší se pouze metody výpočtu.

### <a name="stepped-calculation-method"></a>Metoda krokového výpočtu

Metoda krokového výpočtu počítá krok za krokem, kde každý řádek nabídky postupně přispívá k rabatu, dokud není dosaženo množství nebo hodnoty prodeje. Kroky mohou být založeny buď na množství, nebo hodnotě prodaného zboží, v závislosti na nastavení pole **Základ** na kartě **Obecné** záložky s náhledem **Podrobnosti správy rabatu**.

Například řádek nabídky je nastaven tak, aby bylo pole **Metoda výpočtu** nastaveno na *Kroková* a pole **Základ** bylo nastaveno na *Hodnota*. Zahrnuje řádky výpočtu, které poskytují následující rabaty:

- **Řádek A:** 10 procent až do 1 000 USD
- **Řádek B:** 25 procent až do 2 500 USD

Pokud je hodnota zakoupeného nebo prodaného zboží 2 000 USD, výsledný rabat 350 USD se vypočítá následujícím způsobem:

- **Rabat (A):** *Prahová hodnota (A)* × *Procento (A)* = 1 000 USD × 10 procent = 100 USD
- **Rabat (B):** (*Prodaná hodnota* - *Prahová hodnota (A)*) × *Procento (B)* = (2 000 USD - 1 000 USD) × 25 procent = 250 USD
- **Celkový rabat:** *Rabat (A)* + *Rabat (B)* = 100 + 250 = 350 USD

Pokud je pole **Základ** nastaveno na *Množství* namísto *Hodnota*, metoda krokového výpočtu funguje podobným způsobem. První krok se používá pro identifikované množství, dokud není dosaženo druhého kroku. Druhý krok se poté použije pro veškeré množství nad prvním krokem, dokud není dosaženo třetího kroku. Tento proces poté pokračuje všemi následujícími kroky.

### <a name="cumulative-calculation-method"></a>Kumulativní metoda výpočtu

Kumulativní metoda výpočtu používá k výpočtu rabatu pouze jeden řádek výpočtu. Pokud je pro řádek nabídky k dispozici více řádků výpočtu, použije se pro celé množství nebo hodnotu řádek výpočtu nejvyšší hodnoty nebo nejvyššího množství, kterého je dosaženo. Stejně jako ostatní metody výpočtu používá kumulativní metoda nastavení pole **Základ** na kartě **Obecné** záložky s náhledem **Podrobnosti správy rabatu** k určení, zda se k výpočtu rabatů použije množství prodeje nebo hodnota prodeje.

Například řádek nabídky je nastaven tak, aby bylo pole **Metoda výpočtu** nastaveno na *Kumulativní* a pole **Základ** bylo nastaveno na *Hodnota*. Zahrnuje řádky výpočtu, které poskytují následující rabaty:

- **Řádek A:** 10 procent až do 1 000 USD
- **Řádek B:** 25 procent až do 2 500 USD

Pokud je hodnota zakoupeného nebo prodaného zboží 2 000 USD, výpočet použije pouze řádek B. Výsledný rabat 500 USD se vypočítá následujícím způsobem:

- **Celkový rabat:** *Prodaná hodnota* × *Rabat (B)* = 2 000 USD × 25 procent = 500 USD

### <a name="rolling-calculation-method"></a>Metoda postupného výpočtu

Metoda postupného výpočtu vypočítá všechny možné řádky výpočtu pro nabídku. Pokud existuje více řádků výpočtu a je dosaženo více než jednoho z nich, budou použity všechny dosažené řádky výpočtu, ale pro každé procento platí horní prahové hodnoty. Stejně jako ostatní metody výpočtu používá postupná metoda nastavení pole **Základ** na kartě **Obecné** záložky s náhledem **Podrobnosti správy rabatu** k určení, zda se k výpočtu rabatů použije množství prodeje nebo hodnota prodeje.

Například řádek nabídky je nastaven tak, aby bylo pole **Metoda výpočtu** nastaveno na *Postupná* a pole **Základ** bylo nastaveno na *Hodnota*. Zahrnuje řádky výpočtu, které poskytují následující rabaty:

- **Řádek A:** 10 procent až do 1 000 USD
- **Řádek B:** 25 procent až do 2 500 USD

Pokud je hodnota zakoupeného nebo prodaného zboží 2 000 USD, výsledný rabat 600 USD se vypočítá následujícím způsobem:

- **Rabat (A):** *Prahová hodnota (A)* × *Procento (A)* = 1 000 USD × 10 procent = 100 USD
- **Rabat (B):** *Prodaná hodnota* × *Procento (B)* = 2 000 USD × 25 procent = 500 USD
- **Celkový rabat:** *Rabat (A)* + *Rabat (B)* = 100 + 500 = 600 USD

### <a name="total-calculation-method"></a>Metoda celkového výpočtu

Celková metoda výpočtu používá k výpočtu rabatu všechny řádky výpočtu. Aplikuje celkové množství pro výpočet rabatu pro každý řádek výpočtu, kterého je dosaženo, a každý řádek výpočtu použije své procento na celou částku. Stejně jako ostatní metody výpočtu používá celková metoda nastavení pole **Základ** na kartě **Obecné** záložky s náhledem **Podrobnosti správy rabatu** k určení, zda se k výpočtu rabatů použije množství prodeje nebo hodnota prodeje.

Například řádek nabídky je nastaven tak, aby bylo pole **Metoda výpočtu** nastaveno na *Celková* a pole **Základ** bylo nastaveno na *Hodnota*. Zahrnuje řádky výpočtu, které poskytují následující rabaty:

- **Řádek A:** 10 procent až do 1 000 USD
- **Řádek B:** 25 procent až do 2 500 USD

Pokud je hodnota zakoupeného nebo prodaného zboží 2 000 USD, výsledný rabat 700 USD se vypočítá následujícím způsobem:

- **Rabat (A):** *Prodaná hodnota* × *Procento (A)* = 2 000 USD × 10 procent = 200 USD
- **Rabat (B):** *Prodaná hodnota* × *Procento (B)* = 2 000 USD × 25 procent = 500 USD
- **Celkový rabat:** *Rabat (A)* + *Rabat (B)* = 200 + 500 = 700 USD
