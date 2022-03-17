---
title: Sestavy hodnot zásob
description: Toto téma vysvětluje postup při nastavení, generování a používání sestav hodnot zásob. Tyto sestavy poskytují podrobnosti o fyzických a finančních množstvích a částkách vašich zásob.
author: banluo-ms
ms.date: 10/19/2021
ms.topic: article
ms.search.form: InventValueProcess, InventValueReportSetup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: banluo
ms.search.validFrom: 2021-10-19
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: d78cde26d238d18744adde9a576552588736e619
ms.sourcegitcommit: 2e554371f5005ef26f8131ac27eb171f0bb57b4e
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/04/2022
ms.locfileid: "8384688"
---
# <a name="inventory-value-reports"></a>Sestavy hodnot zásob

[!include [banner](../includes/banner.md)]

Sestavy hodnoty zásob poskytují podrobnosti o fyzických a finančních množstvích a částkách vašich zásob. Sestavy můžete zobrazit mnoha různými způsoby. Můžete například zobrazit součty nebo transakce, nebo filtrovat podle položek či časového rozsahu. Můžete zobrazit hodnoty nákladů prodaného zboží (COGS) nebo hodnoty nedokončené výroby (NV) a nastavit další možnosti.

Sestavy hodnoty zásob vám umožňují provádět následující úkoly:

- Odsouhlasení mezi hlavní knihou a inventářem.
- Prohlédnout si zásoby a hodnoty za konkrétní období.
- Vytvářet konfigurace sestav, které jsou přizpůsobeny konkrétnímu účelu.
- Uložit konfigurace sestav, abyste je mohli použít vícekrát.
- Přidat rozsahy k filtrování dat při spuštění sestavy.

## <a name="types-of-inventory-value-report"></a>Typy sestav hodnot zásob

Existují dva typy sestav hodnot zásob: **Hodnota zásob** (standardní sestava) a **Úložiště sestavy hodnot zásob**.

### <a name="standard-inventory-value-report"></a>Standardní sestava hodnot zásob

Standardní sestava **Hodnota zásob** je jednoduchá sestava, která vám umožní vybrat do ní zahrnuté informace, a poté tyto informace zobrazí na obrazovce. Neuloží výsledky. Rovněž neposkytuje interaktivní funkce pro filtrování, zobrazení detailů, procházení nebo exportování. Z těchto důvodů vám doporučujeme používat místo ní ve většině případů sestavu **Úložiště sestavy hodnot zásob**.

### <a name="inventory-value-report-storage-report"></a>Sestava Úložiště sestavy hodnot zásob

Sestava **Úložiště sestavy hodnot zásob** poskytuje výstup buď jako interaktivní stránku v Microsoft Dynamics 365 Supply Chain Management, nebo jako exportovaný dokument v jednom z několika formátů.

Pokud zobrazíte sestavu ve svém prohlížeči, sloupce a agregované zůstatky jsou v závislosti na vámi konfigurovaném rozvržení dynamicky upravovány. Výsledky můžete řadit, filtrovat, přecházet k podrobnostem atd.

Výsledky sestavy se ukládají do datové entity data **Hodnota zásob**. Z tohoto důvodu můžete výsledky filtrovat a exportovat do formátu CSV nebo Microsoft Excel.

Sestava **Úložiště sestavy hodnot zásob** je užitečná, pokud výstup obsahuje mnoho řádků. Máte například 50 000 položek a 300 úložišť bylo vytvořeno jako sklady. V takovém případě, pokud vyžádáte konečné zůstatky zásob podle zboží, pracoviště a skladu, bude výstup obsahovat mnoho řádků.

> [!NOTE]
> Sestava **Úložiště sestavy hodnot zásob** nezahrnuje mezisoučty definované v jejím rozvržení. Nezahrne také zůstatky hlavní knihy, i když jsou tyto zůstatky definovány v rozvržení sestavy. Odsouhlasení do hlavní knihy je nutné provést pomocí předvah. Nicméně standardní sestava **Hodnota zásob** tyto mezisoučty a zůstatky obsahuje.

## <a name="turn-the-inventory-value-report-storage-feature-on-or-off"></a>Zapnutí nebo vypnutí sestavy Úložiště sestavy hodnot zásob

Od verze Supply Chain Management 10.0.25 je tato funkce ve výchozím nastavení zapnuta. Správci mohou tuto funkci zapnout nebo vypnout vyhledáním funkce *Úložiště sestavy hodnot zásob* v pracovním prostoru [Správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

## <a name="define-inventory-value-report-configurations"></a><a name="report-configuration"></a>Definujte konfigurace sestavy hodnoty zásob

Na stránce **Sestavy hodnot zásob** nastavte obsah, který je zahrnut do různých typů sestav o hodnotě zásob. Můžete definovat libovolný počet typů sestav. Pokaždé, když vygenerujete kterýkoli typ sestavy hodnoty zásob, vyberete typ sestavy.

1. Přejděte do nabídky **Správa nákladů \> Nastavení účetních zásad skladů \> Sestavy hodnot zásob**.
1. Proveďte jeden z následujících kroků:

    - Chcete-li upravit existující sestavu, vyberte ji v podokně seznamu a poté vyberte **Upravit** v podokně akcí.
    - Chcete-li novou sestavu, vyberte v podokně Akce možnost **Nová**.

1. V záhlaví nové nebo vybrané sestavy nastavte následující pole:

    - **ID** – Zadejte krátký identifikátor sestavy. Tato hodnota musí být jedinečná mezi všemi konfiguracemi sestav hodnot zásob. Po uložení nové konfigurace ji nelze upravit.
    - **Název** – Zadejte popisný název sestavy.

1. Pokud vytváříte novou konfiguraci sestavy, vyberte v podokně akcí příkaz **Uložit**, abyste zpřístupnili zbývající pole.
1. Na pevné záložce **Obecné** zadejte následující pole:

    - **Časový interval** – Vyberte předdefinovaný časový interval. Tento časový interval můžete přepsat při spuštění sestavy.
    - **Rozsah** – Vyberte jednu z možností *Datum zaúčtování* nebo *Čas transakce* v závislosti na datu a čase, který by měl být použit při načítání záznamů pro sestavu.
    - **Sada dimenzí** – Vyberte sadu dimenzí, pro kterou chcete spustit data. (Dimenze jsou definovány v hlavní knize.) Můžete například spustit data pro *Hlavní účet* nebo pro *Hlavní účet + Obchodní jednotku*. Vybraná sada dimenzí nesmí obsahovat více než dvě dimenze. Další informace naleznete v tématu [Sady finančních dimenzí](../../finance/general-ledger/financial-dimension-sets.md).

1. Na záložce s náhledem **Sloupce** zadejte následující pole. Tato pole řídí sloupce, které sestava obsahuje, a typy dat v těchto sloupcích.

    - **Zásoby** – Nastavte tuto možnost na *Ano*, chcete-li zobrazit hodnoty zásob. Tyto hodnoty pak můžete odsouhlasit se zůstatky účtů hlavní knihy.
    - **NV** – Nastavte tuto možnost na *Ano*, chcete-li zobrazit hodnoty nedokončené výroby. Tyto hodnoty pak můžete odsouhlasit se zůstatky účtů NV v hlavní knize. Když nastavíte tuto možnost na *Ano*, sestava zobrazí pouze fyzická množství a množství zásob, které mají stav NV. Výrobní zakázky, které mají status NV, byly vybrány nebo hlášeny jako dokončené, ale nebyly ukončeny.
    - **Odložené COGS** – Nastavte tuto možnost na *Ano*, chcete-li zobrazit sloupec, který ukazuje fyzické množství a částky zásob pro odložené COGS. Odložené COGS se zobrazují pomocí fyzických množství a částek, protože kompenzují množství a částky na dodacích listech.
    - **COGS** – Nastavte tuto možnost na *Ano*, chcete-li zobrazit sloupec, který zobrazuje finanční množství a částky pro COGS. COGS se zobrazují pomocí finančních množství a částek, protože kompenzují množství a částky na fakturách.
    - **Zisk a ztráta** – Nastavte tuto možnost na *Ano*, chcete-li zobrazit sloupec, který ukazuje finanční částku zaúčtovanou do výkazů zisků a ztrát pro zásoby.
    - **Tisk kumulativních hodnot účtu pro porovnání** – Nastavte tuto možnost na *Ano*, chcete-li zobrazit sloupec, který ukazuje zůstatek účtu hlavní knihy. Tímto způsobem nebudete muset kontrolovat zůstatek v předvaze. Tato možnost funguje pouze ve standardní sestavě **Hodnota zásob**, ne v sestavě **Úložiště sestavy hodnot zásob**. Po nastavení této možnosti na *Ano* musíte pomocí následujících polí zadat všechny účty hlavní knihy, které chcete vypsat, v závislosti na možnostech **Finanční pozice**, které jste povolili.

        > [!NOTE]
        > Pokud vyberete *součtový* účet pro kterékoli z těchto polí, zobrazí se jak částka každého účtu zásob, který je zahrnut do součtového účtu, tak částka součtového účtu.

        - **Účet zásob** – Zadejte účet hlavní knihy, jehož informace o zásobách se mají zobrazovat. (Obě možnosti **Zásoby** a **Tisk kumulativních hodnot účtu pro porovnání** musejí být nastaveny na *Ano* .)
        - **Účet NV** – Zadejte účet hlavní knihy, jehož informace o nedokončené výrobě se mají zobrazovat. (Obě možnosti **NV** a **Tisk kumulativních hodnot účtu pro porovnání** musejí být nastaveny na *Ano* .)
        - **Účet odložených COGS** – Zadejte účet hlavní knihy, jehož informace o odložených COGS se mají zobrazovat. (Obě možnosti **Odložené COGS** a **Tisk kumulativních hodnot účtu pro porovnání** musejí být nastaveny na *Ano* .)
        - **Účet COGS** – Zadejte účet hlavní knihy, jehož informace o COGS se mají zobrazovat. (Obě možnosti **COGS** a **Tisk kumulativních hodnot účtu pro porovnání** musejí být nastaveny na *Ano* .)

    - **Shrnout fyzické a finanční hodnoty** – Nastavte tuto možnost na *Ano*, chcete-li zobrazit sloupec ukazující celkové množství zásob a částku zásob (souhrn fyzických i finančních hodnot zásob). Pokud je tato možnost nastavena na *Ne*, sestava zobrazí fyzické i finanční hodnoty zásob.
    - **Zahrnout nezaúčtované do hlavní knihy** Nastavte tuto možnost na *Ano*, chcete-li zobrazit sloupec ukazující transakce, které nebyly nikdy zaúčtovány do hlavní knihy. Transakce pro následující typy položek nemusí být zaúčtovány do hlavní knihy:

        - Přijaté a dosud nevyfakturované položky, když je možnost **Zaúčtovat fyzické zásoby** pro příslušnou skupinu modelů položek vypnuta.
        - Přijaté a dosud nevyfakturované položky, když je možnost **Zaúčtovat příjemku produktu do hlavní knihy** vypnuta na záložce s náhledem **Příjem produktu** na kartě **Všeobecné** ve stránce **Parametry závazků** (**Závazky \> Nastavení \> Parametry závazků**).

    - **Vypočítat průměrné náklady na jednotku** – Nastavte tuto možnost na *Ano*, chcete-li zobrazit sloupec s průměrnými náklady na jednotku. Průměrné náklady na jednotku jsou celková částka dělená celkovým množstvím.
    - **Celkové množství a hodnota** – Nastavte tuto možnost na *Ano*, chcete-li zobrazit sloupce ukazující celkové množství fyzických zásob (a finanční množství) a celkovou částku fyzických zásob (a finanční částky). Tuto možnost můžete nastavit na *Ano*, pouze když je možnost **Shrnout fyzické a finanční hodnoty** nastavena na *Ne*.
    - **Dimenze zásob** – V této mřížce zapněte zaškrtávací políčko **Zobrazit** u každé dimenze, kterou chcete v sestavě zobrazit. V sestavě se zobrazí pouze dimenze, které mají zapnutou možnost **Finanční zásoby**. Ostatní dimenze zobrazí pouze prázdné sloupce. U dimenzí, které vyberete k zobrazení, můžete zapnutím políčka **Součet** zahrnout i součtové údaje.
    - **ID zdroje** – Nastavte možnost **Zobrazit** na *Ano*, chcete-li zobrazit sloupec identifikující položku pro každý řádek. Nastavte možnost **Součet** na *Ano*, chcete-li zahrnout i součty. V závislosti na typu položky, která je uvedena v každém řádku, zobrazuje sloupec jeden z následujících typů informací:

        - **Materiál** – Sloupec ukazuje hodnotu pole `ItemID` pro příslušný záznam materiálu.
        - **Práce** – Sloupec ukazuje hodnotu pole `WorkCenterID` pro příslušný záznam práce.
        - **Nepřímé náklady** – Sloupec ukazuje hodnotu pole `CodeID` pro příslušný záznam nákladů.

        Pokud je možnost **Zobrazit** nastavena na *Ne* pro pole **ID zdroje** i **Skupina zdrojů**, uvidíte pouze celkovou hodnotu zásob, která je založena na dimenzích zásob, které jste vybrali.

    - **Skupina zdrojů** – Nastavte možnost **Zobrazit** na *Ano*, chcete-li zobrazit sloupec identifikující skupinu zdrojů pro každý řádek. Nastavte možnost **Součet** na *Ano*, chcete-li zahrnout i součty. V závislosti na typu položky, která je uvedena v každém řádku, zobrazuje sloupec jeden z následujících typů informací:

        - **Materiál** – Sloupec ukazuje hodnotu pole `ItemGroup` pro příslušný záznam materiálu.
        - **Práce** – Sloupec ukazuje hodnotu pole `WorkcenterGroup` pro příslušný záznam práce.
        - **Nepřímé náklady** – Sloupec ukazuje hodnotu pole `CostGroup` pro příslušný záznam nákladů. (Hodnota `CostGroupType` musí být *Nepřímé*.)

        Pokud je možnost **Zobrazit** nastavena na *Ne* pro pole **ID zdroje** i **Skupina zdrojů**, uvidíte pouze celkovou hodnotu zásob, která je založena na dimenzích zásob, které jste vybrali.

1. Na záložce s náhledem **Řádky** nastavte následující pole. Tato pole umožňují přidat do sestavy odpovídající podsekce související s NV nebo je odstranit.

    - **Materiál** – Nastavte tuto možnost na *Ano*, chcete-li zobrazit informace o materiálech. *Materiál* je výchozí typ zdroje, protože materiály musí být zahrnuty ve všech konfiguracích sestav, aby se vytvořil spolehlivý výstup.
    - **Práce** – Nastavte tuto možnost na *Ano*, chcete-li zobrazit mzdové náklady NV.
    - **Nepřímé náklady** – Nastavte tuto možnost na *Ano*, chcete-li zobrazit nepřímé náklady NV.
    - **Přímý outsourcing** – Nastavte tuto možnost na *Ano*, chcete-li zobrazit náklady na přímý outsourcing u NV. Tyto informace se hodí pro zadávání subdodávek.
    - **Úroveň detailů** – Vyberte možnost zobrazení pro sestavu:

        - *Transakce* – Zobrazení všech relevantních transakcí v sestavě. Pamatujte, že při prohlížení sestav obsahujících velký objem transakcí můžete zaznamenat problémy s výkonem. Pokud tedy chcete použít tuto možnost zobrazení, doporučujeme použít sestavu **Úložiště sestavy hodnot zásob**.
        - *Součty* – Zobrazit celkový výsledek.

    - **Zahrnout počáteční zůstatek** – Nastavte tuto možnost na *Ano*, chcete-li zobrazit počáteční zůstatek. Tato možnost je dostupná pouze v případě, kdy je pole **Úroveň detailů** nastaveno na *Transakce*.

## <a name="generate-an-inventory-value-report-storage-report"></a>Generování sestavy Úložiště sestavy hodnot zásob

Chcete-li vytvořit a uložit sestavu **Úložiště sestavy hodnot zásob**, postupujte takto.

1. Přejděte na **Správa zásob \> Dotazy a sestavy \> Úložiště sestavy hodnot zásob**.
1. V podokně akcí zvolte **Nový**.
1. V dialogovém okně **Hodnota zásob** na záložce s náhledem **Parametry** nastavte následující pole:

    - **Název** – Zadejte jedinečný název sestavy.
    - **ID** – Vyberte [konfiguraci sestavy hodnoty zásob](#report-configuration), kterou chcete použít pro sestavu. Konfigurace stanoví možnosti pro sloupce a řádky, které budou zahrnuty do vaší sestavy.
    - **Časový interval** – Pomocí polí v této části definujte, které záznamy budou zahrnuty do zprávy. Chcete-li definovat časový interval, můžete buď vybrat přednastavený rozsah (relativně k datu generování sestavy) v poli **Kód časového intervalu**, nebo vybrat konkrétní data v polích **Od data** a **Do data**.

1. Na záložce s náhledem **Záznamy k zahrnutí** nastavte filtry a omezení, která definují, která data mají být do sestavy zahrnuta. Výběrem možnosti **Filtr** zobrazíte se standardní dialogové okno editoru dotazu, kde můžete definovat kritéria výběru, kritéria řazení a spojení. Pole fungují stejně jako u jiných typů dotazů v Supply Chain Management. Všechny tyto filtry se použijí na transakce zásob, ale ne na zůstatek hlavní knihy. Mějte toto chování na paměti při nastavování filtrů. V opačném případě můžete zaznamenat nesrovnalosti mezi inventářem a hlavní knihou.
1. N záložce s náhledem **Spustit na pozadí** určete, kdy a jak často bude sestava generována. Pole fungují stejně jako u jiných typů [prací na pozadí](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) v Supply Chain Management.

    > [!NOTE]
    > Tato sestava se vždy spustí jako součást dávkové úlohy.

1. Vyberte **OK**, pokud chcete použít své nastavení a zavřete dialogové okno.

Po dokončení dávkové úlohy se sestava zobrazí na stránce **Úložiště sestavy hodnot zásob**. Možná bude nutné pro zobrazení sestavy aktualizovat stránku.

> [!IMPORTANT]
> Ve vybrané konfiguraci sestavy hodnoty zásob můžete obdržet nesprávný počáteční zůstatek, pokud vyberete stejné datum v polích **Od data** a **Do data**, a pokud také nastavíte možnost **Zahrnout počáteční zůstatek** na *Ano*.

## <a name="explore-an-inventory-value-report-storage-report"></a>Prozkoumání sestavy Úložiště sestavy hodnot zásob

Po vygenerování sestavy ji můžete kdykoli zobrazit a prozkoumat následujícím způsobem.

1. Přejděte na **Správa zásob \> Dotazy a sestavy \> Úložiště sestavy hodnot zásob**.
1. V seznamu vyberte sestavu. Stránka zobrazuje podrobnosti o [konfiguraci sestavy hodnoty zásob](#report-configuration), která byla použita k vygenerování vybrané sestavy.
1. Výběrem možnosti **Zobrazit detaily** v podokně akcí zobrazíte obsah sestavy.
1. Prozkoumejte sestavu pomocí některého z následujících kroků:

    - Stejně jako u většiny standardních formulářů v Supply Chain Management můžete vybrat téměř libovolné záhlaví sloupce, podle jehož hodnot chcete seřadit nebo filtrovat mřížku.
    - Pro filtrování sestavy podle libovolné hodnoty v několika dostupných sloupcích vyberte pole **Filtr**.
    - Pomocí nabídky Zobrazení (nad polem **Filtr**) uložte a načtěte oblíbené kombinace možností řazení a filtrování.

## <a name="export-an-inventory-value-report-storage-report"></a>Export sestavy Úložiště sestavy hodnot zásob

Každá generovaná sestava je uložena v datové entitě **Hodnota zásob**. Pomocí standardních funkcí Supply Chain Management můžete exportovat data z této entity do libovolného podporovaného formátu dat, včetně formátu CSV nebo Excel.

Následující příklad ukazuje, jak exportovat sestavu **Úložiště sestavy hodnot zásob**.

1. Přejděte do nabídky **Správa systému \> Pracovní prostory \> Správa dat**.
1. V oddílu **Import/export** vyberte dlaždici **Export**.
1. Na stránce **Export**, která se zobrazí, nastavte úlohu exportu. Nejprve zadejte název skupiny dané úlohy.
1. V části **Vybrané entity** vyberte **Přidat entitu**.
1. V zobrazeném dialogovém okně nastavte následující pole:

    - **Název entity** – vyberte *Hodnota zásob*.
    - **Formát cílových dat** – vyberte formát, do kterého mají být exportována data.

1. Volbou **Přidat** přidejte nový řádek a volbou **Zavřít** zavřete dialogové okno.
1. Obvykle se exportuje vždy jedna sestava. Při exportu jedné sestavy nastavte filtr pro řádek, který jste právě přidali do dialogového okna **Dotaz**. Tímto způsobem můžete definovat, která sestava z entity **Hodnota zásob** bude zahrnuta do exportu. Pomocí těchto kroků nastavíte následující možnosti filtru pro export jedné sestavy:

    1. Na kartě **Rozsah** vyberte možnost **Přidat** a přidejte řádek.
    2. Pole **Tabulka** nastavte na *Hodnota zásob*.
    3. Pole **Odvozená tabulka** nastavte na *Hodnota zásob*.
    4. Pole **Pole** nastavte na pole, podle kterého chcete filtrovat. Obvykle použijete pole **Název spuštění** nebo **Čas spuštění**.
    5. Ve vybraném poli nastavte pole **Kritéria** na hodnotu, kterou chcete vyhledat. (Pokud jste v předchozím kroku vybrali pole **Název spuštění**, tato hodnota bude názvem sestavy. Pokud jste vybrali pole **Čas spuštění**, názvem bude čas, kdy byla sestava vygenerována.)
    6. V případě potřeby přidejte na kartu **Rozsah** další řádky, dokud neidentifikujete jedinečnou sestavu, kterou hledáte.

1. Volbou **OK** uložte svá nastavení a zavřete dialogové okno.
1. Nastavení exportu uložíte výběrem možnosti **Uložit**.
1. Na kartě **Možnosti exportu** volbou **Exportovat nyní** vygenerujte exportovaný soubor.
1. Na otevřené stránce **Souhrn spuštění** můžete zobrazit stav úlohy exportu a seznam exportovaných entit. V části **Stav zpracování entity** vyberte v seznamu entitu **Hodnota zásob** a poté volbou **Stáhnout soubor** stáhněte data, který byla exportována z této entity.

Další informace o tom, jak používat správu dat k exportu dat, naleznete v tématu [Přehled úloh importu a exportu dat](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md).

## <a name="generate-a-standard-inventory-value-report"></a>Generování standardní sestavy hodnot zásob

Pro vytvoření standardní sestavy **Hodnota zásob** použijte následující postup.

1. Přejděte na **Správa nákladů \> Dotazy a sestavy \> Skladové účetnictví – sestavy stavů \> Hodnota zásob**.
1. V dialogovém okně **Sestava hodnoty zásob** nastavte na záložce s náhledem **Parametry** následující pole:

    - **Název** – Zadejte jedinečný název sestavy.
    - **ID** – Vyberte [konfiguraci sestavy hodnoty zásob](#report-configuration), kterou chcete použít pro sestavu. Konfigurace stanoví možnosti pro sloupce a řádky, které budou zahrnuty do vaší sestavy.
    - **Časový interval** – Pomocí polí v této části definujte, které záznamy budou zahrnuty do zprávy. Chcete-li definovat časový interval, můžete buď vybrat přednastavený rozsah (relativně k datu generování sestavy) v poli **Kód časového intervalu**, nebo vybrat konkrétní data v polích **Od data** a **Do data**.

1. Na záložce s náhledem **Záznamy k zahrnutí** nastavte filtry a omezení, která definují, která data mají být do sestavy zahrnuta. Výběrem možnosti **Filtr** zobrazíte se standardní dialogové okno editoru dotazu, kde můžete definovat kritéria výběru, kritéria řazení a spojení. Pole fungují stejně jako u jiných typů dotazů v Supply Chain Management.
1. N záložce s náhledem **Spustit na pozadí** určete, kdy a jak často bude sestava generována. Pole fungují stejně jako u jiných typů [prací na pozadí](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) v Supply Chain Management.
1. Vyberte **OK**, pokud chcete použít své nastavení a zavřete dialogové okno. Zobrazí se sestava.

## <a name="reading-inventory-value-reports"></a>Čtení sestav hodnot zásob

Tato část obsahuje návody, jak číst sestavy hodnoty zásob a chápat jejich obsah.

Supply Chain Management podporuje následující dva důležité koncepty, které se týkají stavu zásob:

- **Finanční aktualizace** – Tento koncept znamená, že transakce zásob jsou již fakturovány. U výrobních zakázek označuje konec výrobní zakázky.
- **Fyzicky aktualizované** – Tento koncept říká, že transakce zásob ještě nebyly vyfakturovány, ale byly přijaty nebo odeslány. U výrobních zakázek to znamená, že byl vyskladněn materiál nebo byla výrobní zakázka vykázána jako dokončená.

Když pochopíte tyto dva koncepty, měli byste chápat následující sloupce ve výstupu sestavy:

- **Zásoby: Finanční množství** – Finančně aktualizované množství.
- **Zásoby: Finanční částka** – Hodnota částky zásob, které byly finančně aktualizovány.
- **Zásoby: Zaúčtované fyzické množství** – Fyzicky aktualizované množství.
- **Zásoby: Zaúčtovaná fyzická částka** – Hodnota částky zásob, které byly fyzicky aktualizovány.
- **Zásoby: Nezaúčtované fyzické množství** – Množství, které má transakce zásob, ale nebylo zaúčtováno do hlavní knihy. Máte například skupinu modelů položek, kde jsou možnosti **Zaúčtovat fyzické zásoby** a **Zaúčtovat finanční zásoby** vypnuté, a máte položku, která je s touto skupinou spojena. Poté vytvoříte nákupní objednávku, přijmete ji a vyfakturujete. Pokud si v tomto okamžiku prohlédnete sestavu hodnoty zásob pro položku, uvidíte, že množství a hodnota na nákupní objednávce jsou zobrazeny ve sloupcích **Zásoby: Nezaúčtované fyzické množství** a **Zásoby: Nezaúčtovaná fyzická částka**.
- **Zásoby: Nezaúčtovaná fyzická částka** – Přehledy můžete nastavit tak, aby zobrazovaly nezaúčtované částky. Pokud však sestavu používáte pro odsouhlasení zásob, tuto hodnotu nepoužívejte. V opačném případě se částka nezaúčtuje do hlavní knihy.
- **Zásoby: Množství** – Celkové součet množství všech sloupců množství v sestavě.
- **Zásoby: Částka** – Celkové součet množství všech sloupců částek v sestavě. Když provádíte odsouhlasení zásob, nepoužívejte tento sloupec, pokud vaše sestava obsahuje sloupec **Zásoby: Nezaúčtovaná fyzická částka**. V tomto případě musíte vyloučit částku **Zásoby: Nezaúčtovaná fyzická částka** z celkové částky.
- **Průměrné náklady na jednotku** – Celková částka dělená celkovým množstvím.

K zobrazení hodnoty a množství zásob obvykle použijete sestavu hodnoty zásob. Někdy však sestava nezobrazí všechny relevantní dimenze inventáře. Pokud nevidíte očekávané dimenze, ověřte následující nastavení:

- Zkontrolujte úložiště položek a skupiny sledovacích dimenzí. V sestavě se mohou zobrazit pouze dimenze, které mají zapnutou možnost **Finanční zásoby**.
- Přejděte do nabídky **Správa nákladů \> Nastavení zásad účtování zásob \> Sestavy hodnoty zásob**, vyberte konfiguraci sestavy, kterou jste použili k vytvoření sestavy, a ujistěte se, že jsou ve sloupci **Zobrazit** vybrány požadované dimenze zásob.

Máte například položku s číslem položky *A0001*. Ve skupině dimenzí úložiště je u finančních zásob povoleno pouze pracoviště. U fyzických zásob jsou povoleny pracoviště i sklad. Ve skupině dimenzí sledování je číslo šarže povoleno pro fyzické zásoby, ale ne pro finanční zásoby. Potom použijete konfiguraci sestavy, kde je vybráno pracoviště, sklad a číslo šarže. Při zobrazení sestavy uvidíte hodnotu pouze pro dané pracoviště. Sloupce pro sklad a číslo šarže jsou prázdné. Jak ukazuje tento příklad, sestavy hodnoty zásob mohou zobrazovat pouze dimenzi zásob, která je povolena pro finanční zásoby.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
