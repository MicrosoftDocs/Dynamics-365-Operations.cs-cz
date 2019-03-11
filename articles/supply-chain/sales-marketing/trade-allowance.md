---
title: Správa obchodních náhrad
description: Toto téma popisuje správu obchodních náhrad pro Microsoft Dynamics 365 for Finance and Operations.
author: t-benebo
manager: AnnBe
ms.date: 08/17/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: t-benebo
ms.search.validFrom: 2018-01-31
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 907d59f850d8d761e2dd4e04bd288a696f00964d
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "318803"
---
# <a name="trade-allowance-management"></a>Správa obchodních náhrad

[!include [banner](../includes/banner.md)]

Správa obchodních náhrad pomáhá společnostem spravovat programy na podporu prodeje, které nabízejí maloobchodní peněžní odměny za "výkonnostní složku", a to pro odběratele, kteří dosáhnou cílový objem a behaviorální cíle. Tato funkce je určena pro společnosti, které se zaměřují na komplexní procesy propagace za účelem zisku, od rozpočtování a přidělení finančních prostředků na promoakce přes vytvoření smlouvy náhrad, vytvoření a zpracování nároků a zpracování plateb po analýzu efektivity propagace.


Tento článek nabízí široký přehled funkce správy obchodních náhrad a seznámí vás s typickou sadu úloh, které jsou součástí správy programu na podporu prodeje. Tato funkce je určena několika typů uživatelů, kteří mají zodpovědnost za provoz a rozhodování a kterým by měla pomoci dosáhnout svých cílů:

- Přidělení volitelných finančních prostředků k vybraným účtům a vytvoření smlouvy o obchodních náhradách pro promoakce na základě zpětných fakturací a jednorázových paušálních plateb (pro odsouhlasenou službu)
- Spuštění vyjednaných smluv na promoakce prostřednictvím probíhajícího prodeje a generování nároků na zpětnou fakturaci
- Výpočet, schválení a zpracování generovaných nároků a jejich předání mezi pohledávky jako odpočty k vyrovnání platby
- Odsouhlasení částečné platby odběratele s odpočtem, který je splatný
- Sledování použití finančních prostředků na promoakce a vyhodnocení ziskovosti a efektivity programu

## <a name="audience-and-purpose"></a>Cílová skupina a účel

Informace v tomto dokumentu jsou určeny osobám s obchodní rozhodovací pravomocí v podniku, kteří zastávají například pozice vedoucího nákupu, vedoucího finančního oddělení (CFO) nebo vedoucího účetního oddělení s těmito odpovědnostmi:

- Souhrnné rozpočty a přiřazení finančních prostředků
- Plánování a analýza prodejních promoakcí
- Správa zaměstnanců, kteří zpracovávající nároky na zpětnou fakturaci, provádějí platby na základě výrobních událostí a vypořádávají částečně platby a odpočty

Osoby v těchto rolích hledají způsoby, jak dosáhnout těchto cílů:

- Lépe využít finančních prostředků na promoakce.
- Flexibilně přizpůsobit různé typy propagačních programů a náhrad.
- Snížit administrativní režii a chyby režie a chyb, které jsou spojeny se sledováním výkonnosti z hlediska promoakcí a zpracováním nároků.
- Vylepšit prognózy cashflow pomocí časového rozlišení pro budoucí závazky.
- Mít kvantifikovaný základ pro probíhající a budoucí jednání s odběrateli o promoakcích.

## <a name="promotional-fund-and-trade-allowance-agreement"></a>Finanční prostředky na promoakce a smlouva o obchodních náhradách

Smlouva o obchodních náhradách je motivační program, kdy jsou za výkonnostní složku nabízeny odměny odběratelům, kteří dosáhnou určitého cílového objemu nebo behaviorálních cílů. Finanční prostředky na promoakce jsou rozpočtované výdaje. Tímto způsobem lze propagační kampaně zaznamenat.

### <a name="promotional-fund"></a>Finanční prostředky na promoakce

Finanční prostředky přiřazené ke smlouvám o obchodních náhradách se zaznamenávají na stránce **Finanční prostředky**. Otevřete stránku **Finanční prostředky**, vyberte **Prodej a marketing** \> **Obchodní náhrady** \> **Finanční prostředky** \> **Finanční prostředky**.

![Stránka Finanční prostředky](./media/trade-allowance-management-funds-page.png "Stránka Finanční prostředky")

Na stránce **Finanční prostředky** můžete zobrazit podrobnosti o finančních prostředcích na promoakce.

Na pevné záložce **Obecné** vidíte období, pro které jsou finanční prostředky platné, a její rozpočtovanou částku. Aby byly finanční prostředky přiděleny ke smlouvě na promoakci, pole **Stav** musí mít hodnotu **Schváleno**.

Pevná záložka **Odběratele** zobrazuje hierarchii odběratelů. Vyberte odběratele, kterým jsou určeny finanční prostředky, a přetáhněte je pod **Finanční prostředky odběratelů**. Tato pevná záložka rovněž zobrazuje, jak je rozdělena celková částka finančních prostředků.

Pevná záložka **Položky** zobrazuje položky, které jsou součástí promoakce.

### <a name="trade-allowance-agreement"></a>Smlouva o obchodních náhradách

Jakmile je hotova definici finančních prostředků, dalším krokem v plánování promoakce je registrace smluv na promoakce (známých jako smlouvy o obchodních náhradách), přidělení finančních prostředků a definování cílů výkonnosti pro jednotlivé výrobní události.

Smlouvy o obchodních náhradách se zaznamenávají na stránce **Smlouvy o obchodních náhradách**. Chcete-li otevřít stránku **Smlouvy o obchodních náhradách**, vyberte **Prodej a marketing** \> **Obchodní náhrady** \> **Smlouvy o obchodních náhradách**.

![Stránka Smlouvy o obchodních náhradách](./media/trade-allowance-management-agreements-page.png "Stránka Smlouvy o obchodních náhradách")

#### <a name="header"></a>Záhlaví

Výběrem **Záhlaví** přepnete na zobrazení Záhlaví.

Na pevné záložce **Obecné** se nachází pole **Objednat do** a **Objednat od**, která definují období platnosti smlouvy. Stav schválení **Interní schválené** pro smlouvu označuje, že smlouva ještě není platná a nelze ji použít při zpracování prodejní objednávky.

Část **Analýza** na pevné záložce **Obecné** obsahuje důležitá pole definující množství a náklady, které se použijí k vyhodnocení promoakce:

- Pole **Základní jednotky** udávají množství produktů, které je nutno prodat vybraným odběratelům před použitím promoakce.
- Hodnota **Vypočítané množství k expedici** se vypočítá na základě hodnoty **Procento zvednutí**, která představuje plánovaný cílový nárůst pro tuto promoakci.
- Pole **Náklady na obchodní náhrady** je vypočteno na základě množství různých událostí ve smlouvě o obchodních náhradách.

Na pevné záložce **Odběratelé** v seznamu vlevo můžete vybrat a zobrazit skupiny odběratelů, které jsou uspořádány jako předdefinované hierarchie. Poté je možné vybrat celou hierarchii nebo konkrétní účty jako cíle pro smlouvu o náhradách.

Na pevné záložce **Položky**, stejně jako na pevné záložce **Položky** na stránce **Finanční prostředky**, jsou do smlouvy přidány produkty za účelem přiřazení jejich prodejů k dohodnuté náhradě.

Na pevné záložce **Finanční prostředky** můžete zobrazit finanční prostředky na promoakce přidružené k této smlouvě. Můžete také zobrazit přidělení nákladů na událost smlouvy. Přidělení nákladů na událost ze 100 % znamená, že tato promoakce bude financována pouze z jednoho finančního prostředku. Eventuálně může smlouva na promoakci čerpat z několika finančních prostředků a použít stejné nebo rozdílové procento přidělení.

#### <a name="lines"></a>Řádky

Dále volbou **Řádky** přepnete na zobrazení Řádky.

Karta **Výrobní události** zobrazují typy událostí pokrytých smlouvou. Existují tři typy: zpětná fakturace, paušál a mimo fakturaci.

Pokud vyberete výrobní událost a poté kartu **Částky**, vyhledají se podrobnosti události.

![Řádky smlouvy o obchodních náhradách](./media/trade-allowance-management-agreements-lines.png "Řádky smlouvy o obchodních náhradách")

V části **řádky obchodních náhrad** určíte rozsahy množství nebo částky, kterých musí odběratel dosáhnout pro získání odměny.

V případě výrobní události pro typ **Zpětná fakturace** definuje horní část karty **Částky** pravidla, která se použijí na zpětnou fakturaci a podle kterých bude vygenerována a zaplacena. Pravidla mohou například vytyčit následující podmínky pro nárok na zpětnou fakturaci:

- Je založena na datu vytvoření prodejní objednávky (hodnota **Typ data výpočtu** je **Vytvořeno**).
- Je vypočítána na základě částky řádky prodejní objednávky před slevou, nikoli na základě čisté částky, která zahrnuje slevy (Hodnota **Zdroj převzetí** je **Brutto**).
- Je založena na množství prodaných produktů, nikoli částce (hodnota **Typ zalomení řádku rabatu** je **Množství**).
- Je vypočítána pro období v měsíci (hodnota **Kumulovat prodeje za** je **Měsíc**). 
- Je vypořádána jako srážka, nikoli pomocí pohledávky (hodnota **Typ platby** je **Srážky u odběratele**).

V případě výrobní události typu **Paušál** zobrazí karta **Částky** množství, které bude zaplaceno odběrateli ve formě odpočtu, když odběratel dosáhne konkrétní výkonnosti. Stav schválení **Otevřeno** označuje, že ještě nebyl vyplacen paušál.

Aby bylo možné smlouvu použít pro prodejní objednávky, které vyhovují podmínkám smlouvy, musí být stav smlouvy **Potvrzeno**. 

## <a name="perform-sales-under-the-planned-merchandising-event-and-generate-bill-back-claims"></a>Realizace prodeje v rámci plánované výrobní události a generování nároků na zpětnou fakturaci

Při vytvoření prodejní objednávky, která obsahuje řádky odpovídající požadavkům smlouvy můžete zobrazit související informace na stránce **Prodejní objednávka** výběrem položek **Řádka prodejní objednávky** \> **Zobrazit** \> **Podrobnosti o ceně**.

Na stránce **Podrobnosti o ceně** a na pevné záložce **Rabaty** může úředník prodeje vidět zpětnou fakturaci z platné smlouvy o obchodních náhradách (je zobrazeno ID rabatového programu) a celkovou částku, která se použije na řádku. Tato částka je rovněž zobrazena v poli **Částka rabatu** v části **Odhad marže** stránky **Podrobnosti o ceně**.

Při zaúčtování prodejní faktury je generován odpovídající nárok na zpětnou fakturaci pro každý řádek faktury.

> [!NOTE]
> Chcete li zobrazit stránku **Podrobností o ceně**, na stránce **Parametry pohledávek** na kartě **Ceny** zaškrtněte políčko **Povolit podrobnosti o ceně**. I

## <a name="process-claims-and-pass-them-as-deductions-to-ar"></a>Zpracování nároků a jejich předání mezi pohledávky jako odpočty

Další kroky procesu zpracování zpětné fakturace jsou kontrola, výpočet a schválení nároků. Poté následuje převod na odpočty.

Pracovní plocha zpětné fakturace označuje místo, kde vlastník smlouvy na promoakci pravidelně kontroluje a zpracovává generované pohledávky. Dále zde správce pohledávek převádí schválené nároky na odpočty nebo pravidelné platby, v závislosti na způsobu platby pohledávky.

Na stránce **Pracovní plocha zpětné fakturace** můžete zkontrolovat řádky nároku. Pokud jsou nároky ve stavu **Přepočítat**, kvůli kumulativnímu účinku musí být přepočítány.

### <a name="recalculate-claims"></a>Přepočítání nároků

Chcete-li přepočítat nároky, v podokně akcí vyberte možnost **Kumulovat**. Potom v dialogovém okně **Kumulovat rabaty** vyberte odběratele.

V důsledku přepočtu program vytvoří nové nároky pro částky, pomocí kterých upraví původní nároky na odpovídající částky pro jednotlivé jednotky. Jeden opravný nárok je generován pro každou jedinečnou kombinaci odběratele, položky, měny, měrné jednotky, dimenzí zásob, finančních dimenzí a skupiny DPH. Tyto opravné nároky mají stejnou referenci na prodejní objednávku a číslo faktury, jako nároky, které jsou upravovány (tzn. nároky, které byly původně vytvořeny z prodejního dokladu). Na rozdíl od původního nároku nemá opravný nárok hodnoty v polích, které popisují částky a množství na řádce prodejní objednávky.

Po dokončení přepočtu se stav nároků změní na **Vypočteno**. Chcete-li schválit nároky, v podokně akcí vyberte možnost **Schválit**.

### <a name="process-claims-and-pass-them-to-ar"></a>Zpracování nároků a jejich předání mezi pohledávky

Nároky jsou nyní připraveny pro zpracování pohledávek. Chcete-li je zpracovat, v podokně akcí vyberte **Zpracovat**. 

Při zpracování nároků se jejich stav změnil na **Označit** a to znamená, že díky zaúčtování deníku (deník, který je zaúčtován, je deník časového rozlišení rabatu, jak je uvedeno v parametrech pohledávek) došlo k následujícím událostem: 

- Nároky byly převedeny do dočasného zůstatku odběratele jako odpočty.
- Na účet časového rozlišení rabatu bylo provedeno připsání představující budoucí odpovědnost směrem k odběrateli.
- Z výdajového účtu rabatu byl proveden odpis v rámci uznání vzniklých nákladů v souvislosti s prodejem.

Pro dokončení procesu musí úředník pro pohledávky zpracovat časové rozlišené odpočty jejich převedením do zůstatku odběratele jako dobropis (závazek). 

Chcete-li zahájit úkol, v podokně akcí na stránce **Odběratel** vyberte **Shromáždit** \> **Vyrovnat transakce**. Poté na stránce **Vyrovnat transakce** vyberte **Funkce** \> **Program zpětné fakturace**. Tato stránka rabatu zobrazuje všechny dříve zpracované nároky na zpětnou fakturaci.

Pokud chcete vytvořit dobropis, u všech řádek zaškrtněte políčko **Označit** a pak vyberte **Funkce** \> **Vytvořit dobropis**.

Při vytvoření dobropisu je zaúčtován deník. (Zaúčtovaný deník je deník spotřeby pohledávek, jak je zadáno v parametrech pohledávek.) V důsledku byla skutečná částka závazku (Dal) přesunuta do zůstatku odběratele. Finančně tato situace znamená, že došlo k následujícím událostem:

- Byl provedeno připsání na účet pohledávek odběratele.
- Bylo provedeno odepsání z účtu časového rozlišení rabatu.

Pokud chcete schválit výrobní událost typu **Paušál**, vyberte událost na stránce **Smlouvy o obchodních náhradách** a poté na kartě **Částka** vyberte **Schválit**.

## <a name="settle-the-deduction-that-is-due-and-the-customer-short-pay-by-using-the-deduction-workbench"></a>Vyrovnání splatného odpočtu a částečné platby odběratele pomocí pracovní plochy odpočtu

Často v očekávání zpětných fakturací odběratel zvolí vybrané faktury s částečnou platbou. Chcete-li zabránit problémům s odsouhlasením plateb v budoucnu, úředník pro pohledávky zaregistruje tyto částečné platby jako odpočty během záznamu skutečných plateb odběratele. Poté lze na pracovní ploše odpočtu tyto odpočty odběratele snadno vyrovnat vůči částkám nároku, které jsou splatné ze strany společnosti.

Pokud chcete částečnou platbu odběratele registrovat v deníku plateb, vyberte položky **Pohledávky** \> **Platby** \> **Deník plateb** a vytvořte nový deník plateb. Poté v podokně akcí zvolte **Odpočty**. Na stránce **Odpočet** stránce můžete vytvořit a sledovat částku, která byla zaplacena částečně.

Manažer kolekce je nyní zodpovědný za vyrovnání otevřené transakce dobropisu a transakce částečné platby vůči sobě, což provede na pracovní ploše odpočtu.

Pro správu odpočtů vyberte položky **Prodej a marketing** \> **Obchodní náhrady** \> **Odpočty** \> **Pracovní plocha odpočtu**. Horní část stránky obsahuje řádky, které představují částečné platby odběratele. Dolní části stránky obsahuje otevřené kreditní transakce odběratele. 

Pokud chcete vyrovnat odpočet vůči otevřené transakci, označte řádku odpočtu a poté na kartě Otevřené transakce označte stejnou řádku. V podokně akcí klikněte na položku Zachování > Spárovat.

Stav původních nároků se nyní změní na **Dokončeno**.

## <a name="analyze-the-effectiveness-of-the-promotion-and-fund-consumption"></a>Analýza efektivity promoakcí a spotřeba finančních prostředků

Chcete-li získat přehled o klíčových statistikách a použití finančních prostředků v rámci daného programu, můžete využít několika sestav a analytických zobrazení, které jsou dostupné v modulu Správa obchodních náhrad.

Na stránce **Aktivita obchodních náhrad** zobrazuje karta **Přehled** hlavní podrobnosti smlouvy o obchodních náhradách. Ostatní karty zobrazují podrobnější informace o souvisejících dokladech, platbách a dalších událostech, které se vztahují k programu.

Karta **Souhrn** zobrazuje celkové množství produktů, které byly prodány v rámci promoakce, fakturovanou částku prodeje a zaplacené zpětné fakturace a paušály.

Karta **Kredity zpětné fakturace** obsahuje podrobnosti o jednotlivých zpětných fakturacích připsaných ve prospěch odběratele.

Analytičtější přehled různých měření výkonu promoakcí najdete v zobrazení Analýza. Do zobrazení Analýza přejdete kliknutím na položky **Prodej a marketingu** \> **Obchodní náhrady** \> **Smlouvy o obchodních náhradách**. V podokně akcí klikněte na položku **Analýza**.  

Analytičtější přehled různých měření výkonu promoakcí najdete v zobrazení Analýza. Do zobrazení Analýza přejdete kliknutím na položky **Prodej a marketingu** \> **Obchodní náhrady** \> **Smlouvy o obchodních náhradách**. V podokně akcí klikněte na položku **Analýza**. 

