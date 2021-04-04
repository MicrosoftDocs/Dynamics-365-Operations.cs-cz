---
title: Rabaty dodavatele
description: Toto téma poskytuje přehled nejběžnějších úloh, které můžete chtít provádět při práci s rabaty dodavatele. Rabaty dodavatele pomáhají společnostem lépe spravovat programy rabatů dodavatelů díky automatizaci úloh potřebných ke správě, sledování a uplatňování nároků na získané rabatů.
author: omulvad
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TAMVendRebateAgreement
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 2012
ms.openlocfilehash: b0bbb97625b9746f8332eb75cac0ab0b904ca7e1
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5246590"
---
# <a name="vendor-rebates"></a>Rabaty dodavatele

[!include [banner](../includes/banner.md)]

Rabaty dodavatele pomáhají společnostem lépe spravovat programy rabatů dodavatelů díky automatizaci úloh potřebných ke správě, sledování a uplatňování nároků na získané rabatů.

Toto téma poskytuje přehled nejběžnějších úloh, které můžete chtít provádět při práci s rabaty dodavatele. Přehled zahrnuje následující úkoly:

- Zkontrolujte podrobnosti smlouvy o rabatu.
- Identifikujte objednávky, na které se rabaty vztahují, a vygenerujte nároky na rabaty.
- Zkontrolujte a schvalte nároky.

## <a name="audience-and-purpose"></a>Cílová skupina a účel

Informace v tomto tématu jsou určeny osobám s obchodní rozhodovací pravomocí v podniku, kteří zastávají například pozice vedoucího nákupu, vedoucího finančního oddělení (CFO) nebo vedoucího účetního oddělení s těmito odpovědnostmi:

- Vyjednávat smlouvy o cenách dodavatele, slevách a rabatech.
- Spravovat personál, který zpracovává nároky na rabat a shromažďuje platby.
- Objednávat zásoby za nejlepší možné ceny.

Osoby na těchto pozicích hledají způsoby, jak dosáhnout různých cílů. Několik příkladů:

- Flexibilně přizpůsobit různé typy dodavatelských propagačních programů a podmínek rabatu.
- Snížit administrativní režii a chyby režie a chyb, které jsou spojeny se sledováním výkonnosti z hlediska promoakcí a zpracováním nároků.
- Vylepšit prognózy cashflow pomocí časového rozlišení pro budoucí pohledávky.
- Mít kvantifikovaný základ pro probíhající a budoucí jednání s dodavateli o rabatech.

## <a name="review-details-of-a-vendor-rebate-agreement"></a>Revidovat podrobnosti smlouvy o rabatu dodavatele.

Smlouva o rabatu dodavatele je záznamem dohody s dodavatelem, který určuje vyjednané smluvní podmínky, při jejichž splnění má společnost nárok na peněžní odměnu za to, že dosáhla přednastavených nákupních cílů. Smlouvy o rabatech dodavatele se zaznamenávají na stránce **Smlouvy o rabatu**.

Chcete-li o stránku **Smlouvy o rabatech dodavatele**, vyberte **Zásobování a zdroje** &gt; **Rabaty dodavatele** &gt; **Smlouvy o rabatu**.

![Nákupní smlouva](media/purchase-agreement.PNG)

Na stránce **Smlouvy o rabatu dodavatele** můžete zobrazit podrobnosti o vyjednaných podmínkách ze smlouvy s dodavatelem.

Záhlaví smlouvy určuje obecné podmínky, které kvalifikují společnost pro rabaty. V důsledku toho informace záhlaví určuje, že dodavatel zaručuje rabat při nákupu konkrétního produktu v konkrétním množství. V záhlaví také určíte možnost jednotky měření rabatu a typ data výpočtu.

- Na kartě **Přehled**, pokud máte řádky s **kódem zboží** nastaveny na *tabulka* pro určení položky, pak smlouva je pro tuto konkrétní položku. Pokud máte řádky s **kódem zboží** nastaveny na *Skupina* nebo *Všech* pro upřesnění položek, bude smlouva o rabatu dodavatele zpracována jednotlivě pro každou položku, která splňuje podmínky pro kód položky, nikoli pro všechny položky, které jsou způsobilé pro kód položky.

- Na kartě **Obecné** v poli **Měrná jednotka (možnost rabatu)** můžete určit, zda měrná jednotka má být podmínkou pro řádek nákupní objednávky, aby došlo k nároku na rabat.

    - **Převést** – Řádek nákupní objednávky vytváří nárok na rabat dodavatele podle smlouvy o rabatu. Získáte rabat bez ohledu na jednotku měření, která je použita na řádku.
    - **Přesná shoda** – Pro získání nároku na rabat musí mít řádek nákupu stejnou jednotky měření, která je určena ve smlouvě.

- Na kartě **Obecné** v poli **Typ data výpočtu** vyberte datum, které slouží k určení, zda k nákupu dochází v době platnosti smlouvy o rabatu.

    - **Vytvořeno** – Použijte datum vytvoření nákupní objednávky.
    - **Požadované dodání** – Použijte datum požadované dodávky.

Na řádcích smlouvy lze určit smlouvu o rabatu dodavatele podrobněji.

- V poli **Kumulovat nákupy podle** můžete nastavit výpočet nároku na rabat. Částku lze nastavit tak, aby závisela na období (týdne, měsíce, roku, doby životnosti nebo přizpůsobené doby). Hodnota **Faktura** označuje, že nárok na rabat bude určen pokaždé, když je řádek nákupní objednávky vyfakturován.
- V poli **Zdroj převzetí** můžete určit základ pro výpočet rabatu.

    - **Hrubý** – Rabat se vypočítá podle hrubé ceny položky.
    - **Čistý** – Rabat se bude počítat podle čisté ceny položky (to znamená ceny po započítání jiných slev).

- Pole **Účet časového rozlišení rabatového programu** a **Výdajový účet rabatového programu** určují čísla účtů, které obdrží časově rozlišené částky rabatu během přechodné fáze mezi zpracováním a schválením.
- Když je možnost **Vyžadováno schválení** nastavena na **Ano**, nárok na rabat musí být schválen předtím, než může být časově rozlišeni nebo proplacen.
- Pole **Typ zalomení řádku rabatu** zobrazuje základ pro rabaty.

    - **Množství** – Rabaty jsou založeny na objemu.
    - **Částka** – Rabaty jsou založeny na částce.

- Na pevné záložce **Řádky** můžete vidět, jak rozdílné úrovně množství mohou být nastaveny pro zaručení různých rabatů. Například na předchozím obrázku pole **Od hodnoty** a **Do hodnoty** označují, že množství produktu mezi 10 a 19 jednotkami zaručí rabat 15 USD na jednu jednotku.

    > [!NOTE]
    > Hodnota **Od hodnoty** je hodnota „včetně“, zatímco hodnota **Do hodnoty** je hodnota „mimo“. Například pole **Typ zalomení řádku rabatu** je nastaveno na **Množství** a zadáte **1** v poli **Od hodnoty** a **3** v poli **Do hodnoty**. V takovém případě se uplatní částka rabatu při zakoupení jedné nebo dvou položek, ale nikoli při zakoupení tří položek.

- V poli **Stav schválení workflowu** označuje hodnota **Schváleno**, že smlouvu lze použít pro nákupní objednávky, které vyhovují podmínkám smlouvy.

## <a name="identify-orders-that-qualify-for-rebates-and-generate-rebate-claims"></a>Identifikace objednávek, na které se rabaty vztahují, a generování nároků na rabaty

Když jsou vytvořeny nákupní objednávky s dodavatelem, se kterým má společnost smlouvu o rabatu, program identifikuje všechny budoucí kreditní platby dodavatele. Pokud nákupní objednávky splňují nárok na rabat, nárok na rabat je generován pro každý řádek objednávky okamžitě při zaúčtování nákupní faktury. Jedná se o automatický proces. Později můžete zkontrolovat očekávané rabaty a zobrazit dopad těchto rabatů na náklady na produkt a marži.

### <a name="view-details-of-rebates-that-are-applied-to-a-purchase-order-line-per-the-vendor-rebate-agreement"></a>Zobrazení podrobností o rabatech, které se použijí na řádek nákupní objednávky podle smlouvy o rabatu dodavatele

1. Na stránce **Nákupní objednávka** vyberte řádek objednávky a poté vyberte **Řádek nákupní objednávky** &gt; **Zobrazit** &gt; **Podrobnosti o ceně**.
2. Na stránce **Podrobnosti o ceně** vyberte pevnou záložku **Rabaty**.

Informace o rabatu je rovněž zobrazeny v poli **Rabat dodavatele** v části **Odhad marže** stránky **Podrobnosti o ceně**.

> [!NOTE]
> Na stránce **Parametry modulu Zásobování a zdroje** na kartě **Ceny** ověřte, zda je možnost **Povolit podrobnosti o ceně** nastavena na **Ano**. Pokud je možnost nastavena na **Ne**, nebudete moci zobrazit rabaty.

## <a name="review-and-approve-claims"></a>Kontrola a schválení nároků

Nároky na rabat, které jsou generovány, představují budoucí platby, které lze očekávat od dodavatele. Před vystavením dobropisu dodavateli obvykle vlastník smlouvy chce zkontrolovat nároky a schválit je. Všimněte si však, že stav nároku určuje, zda je nárok připraven projít schvalovacím procesem.

### <a name="the-status-of-claims-and-the-effect-on-the-approval-process"></a>Stav nároků a vliv na schvalovací proces

Když je nárok vygenerován, je jeho stav nastaven na **K výpočtu**, pokud je rabat zaručen na kumulativním základu, nebo **Vypočteno**, pokud je rabat zaručen podle faktury. Pokud je stav nároku **K výpočtu**, musí projít procesem výpočtu, který provádí funkce Kumulovat. Pouze nároky se stavem **Vypočteno** lze zahrnout do schvalovacího procesu.

> [!NOTE]
> Pokud je možnost **Vyžadováno schválení** na smlouvě o rabatu dodavatele nastavena na **Ne**, žádné vygenerované nároky nebudou mít stav **Schváleno**. Schválení je povinné pro nároky, které jsou garantovány na kumulativním základu.

### <a name="approve-claims-and-view-postings-and-invoice-details"></a>Schválení pohledávek a zobrazení zaúčtování a podrobností o fakturách

Po schválení nároků je lze zpracovat podle závazků. Je automaticky vygenerován dobropis (faktura dodavatele) pro částku nároku na rabat. K zůstatku dodavatele lze poté přidat kredit a tým pohledávek ho může zahrnout do procesu pravidelných vyrovnání.

1. Vyberte **Zásobování a zdroje** &gt; **Rabaty dodavatele** &gt; **Nároky na rabat** a otevřete nárok na rabat.
2. Zavřete nárok na rabat.
3. Označte nárok a potom vyberte v podokně akcí **Schválit**.
4. Na stránce požadavků v poli **Dodavatel** vyberte dodavatele, od kterého máte oprávnění přijmout rabat, a pak vyberte **OK**.

    Deník časového rozlišení rabatu se zaúčtuje pro částku nároku. Toto zaúčtování zapisuje na vrub účtu pohledávek časově rozlišených rabatů dodavatele pro očekávaný kredit dodavatele a připisuje prozatímní účet přijatých časově rozlišených rabatů dodavatele k očekávanému zisku.

    ![Zpráva](media/message.png)

5. V seznamu rabatů vyberte řádek a poté vyberte v podokně akcí **Transakce rabatu** pro zobrazení a přechod na číslo dávky deníku pro toto zaúčtování časově rozlišeného rabatu.

    Abyste přesunuli nároky do běžného procesu pohledávek, musí úředník pohledávek nyní dokončit zpracování nároku na rabat spuštěním funkce Zpracovat.

6. V podokně akcí zvolte **Zpracovat** a poté vyberte **Filtr**. V poli **Kritéria** pro pole **Účet dodavatele** vyberte dodavatele, pro kterého se mají zpracovat nároky na rabat, zvolte další příslušné filtry a zvolte **OK**.

    Panely zpráv a skutečnost, že stav je změněn na **Dokončeno**, označují, že došlo k následujícím událostem:

    - Zaúčtování deníku časového rozlišení rabatu stornovalo předchozí dočasné částky na pohledávce časového rozlišení a účtech výdajů.
    - Byla vytvořena faktura dodavatele (dobropis) pro částku rabatu.

        > [!NOTE]
        > Nastavení možnosti **Ruční zaúčtování faktury** na kartě **Rabatový program** stránky **Parametry modulu Zásobování a zdroje** určuje, zda je faktura dodavatele zaúčtována ručně nebo automaticky v rámci zpracování nároku.

    - Při zaúčtování faktury dodavatele, ručním nebo automatickým, bude částka připsána k tíži účtu závazků dodavatele a připsána k dobru účtu přijatých pohledávek náhrad a slev.

        > [!NOTE] 
        > Číslo účtu přijatých slev a náhrad je určeno pro kategorii zásobování, použitou pro rabat na řádku nákupní faktury. Kategorie zásobování je zase nastavena na kartě **Rabatový program** stránky **Parametry modulu Zásobování a zdroje** stránky.

7. V seznamu rabatů vyberte řádek a poté vyberte v podokně akcí **Transakce rabatu** pro zobrazení a přechod na číslo dávky deníku pro toto zaúčtování časově rozlišeného rabatu a též pro číslo faktury dodavatele.
8. Vyberte řádek pro transakci faktury dodavatele a poté vyberte v podokně akcí **Faktura dodavatele**. Když je faktura dodavatele zaúčtována, zobrazí se deník faktur. V opačném případě se zobrazí faktura dodavatele jako čekající faktura dodavatele, které vyžaduje ruční zaúčtování.

    Řádek faktury určuje podrobné informace o faktuře dodavatele pro kategorii zásobování **Provize a rabaty**.

9. Na stránce **Všichni dodavatelé** vyberte dodavatele, od kterého obdržíte rabat, a poté vyberte v podokně akcí **Transakce**. Najděte řádek pro fakturu. Částka rabatu byla nyní přidána k zůstatku dodavatele.

## <a name="summary"></a>Souhrn

Proces zpracování rabatů dodavatele zahrnuje více úloh ručního sledování, což je často únavné. Díky automatizaci těchto úloh vám může funkce správy rabatů dodavatele pomoci procházet následujícími procesy:

- Generování přesných nároků na rabat
- Časové rozlišení očekávaných pohledávek a dočasného zisku v hlavní knize
- Aktualizace zůstatku dodavatele a výsledovky se splatnou úhradou


[!INCLUDE[footer-include](../../includes/footer-banner.md)]