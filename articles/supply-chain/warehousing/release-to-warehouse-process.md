---
title: Uvolnit do skladu
description: Toto téma poskytuje podrobnosti o procesu uvolnění do skladu. Popisuje entity, které jsou vytvořeny při uvolnění objednávky do skladu, a možnosti, které můžete použít k zahájení procesu.
author: mirzaab
ms.date: 8/13/2021
ms.topic: article
ms.search.form: WHSReleaseToWarehouse, WHSReleaseToWarehouseSalesOrder, WHSReleaseToWarehouseTransferOrder, WHSLoadPlanningWorkbench, WHSWaveTemplateTable, WHSWorkTemplateTable, WHSLocDirTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-08-13
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 3269bf3f8a5475fb85e6b51514db29006be9aab1
ms.sourcegitcommit: b52ff5dfd32580121f74a5f262e5c2495e39d578
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/03/2022
ms.locfileid: "8376201"
---
# <a name="release-to-warehouse"></a>Uvolnit do skladu

[!include [banner](../../includes/banner.md)]

Toto téma poskytuje podrobnosti o procesu uvolnění do skladu. Popisuje entity, které jsou vytvořeny při uvolnění objednávky do skladu, a možnosti, které můžete použít k zahájení procesu.

## <a name="release-to-warehouse-overview"></a>Přehled uvolnění do skladu

Uvolnění do skladu je proces přípravy zásob k odeslání. Když uvolníte objednávku do skladu, systém vytvoří řádky nákladů a zásilky. Pokud je nastaveno automatické zpracování ve vlnách, vytvoří se také zatížení a požadovaná práce. Konfigurace zahrnutých entit závisí na nastavení systému. Tato část tématu shrnuje entity, které jsou vytvořeny během procesu uvolnění do skladu, a systémová nastavení, která je definují.

*Dodávka* je skupina řádků prodejní objednávky nebo převodní objednávky pro stejného zákazníka nebo stejnou dodací adresu.

*Vytížení* je skupina řádků prodejní nebo převodní objednávky, které jsou seskupeny dohromady a které obvykle vycházejí na jednom nákladním vozidle, železničním voze nebo jiném způsobu dopravy. Může mít jednu nebo více zásilek. Vytížení můžete vytvořit ručně přidáním řádků objednávky do nového nákladu. V tomto případě jsou řádky objednávky přiřazeny k nákladu před zahájením procesu uvolnění do skladu a lze je uvolnit pouze ze stránky **Workbench pro plánování vytížení**.

*Práce* ve skladu je jakákoli skladová operace, kterou provádí pracovník skladu. Obvykle pracovní operace ve skladu sestávají z nejméně dvou po sobě jdoucích akcí: skladoví pracovníci vyskladní zásoby na skladě na jednom místě a převedou vyskladněné zásoby v jiném skladovém místě.

Když jsou objednávky uvolněny do skladu, systém vytvoří *řádky nákladů* a seskupí je do zásilek. Proces konsolidace zásilek umožňuje automatizovanou konsolidaci zásilek během procesu uvolnění do skladu. - Další informace viz [Zásady konsolidace dodávek](about-shipment-consolidation-policies.md).

Systém používá *vlny* k vytvoření vychystávacích prací a nákladů pro dodávku. *Šablona vlny* musí být k dispozici pro typ vlny, kterou chcete vytvořit, a pro sklad řádku objednávky. Šablony vlny typu *Expedice* – se používají k expedici položek pro prodejní objednávky a převodních příkazů.

Každá šablona vlny obsahuje *vlnové metody*. Vlnové metody provádějí akce, jako je vytváření prací pro vlnu nebo vytváření zatížení. Šablona vlny pro vlny expedice může například obsahovat metody vytváření nákladů, přidělování řádků k vlnám, doplnění a vytvoření výdeje pro vlnu. Šablona vlny zavádí nastavení definující, jak bude vlna generována a zpracována, včetně kroků, které je třeba provést ručně a které se provádějí automaticky. Další informace naleznete v tématu [Šablony vlny](wave-templates.md). V závislosti na konfiguraci šablony vlny se tedy buď vlna automaticky vytvoří, zpracuje a uvolní při uvolnění objednávky do skladu, nebo se některé nebo všechny tyto akce provedou ručně po vydání do skladu.

Když je vlna zpracována, systém vytvoří vychystávací práci na základě vhodné *pracovní šablony* a *lokalizační směrnice*, a zpřístupňuje tuto funkci na mobilních zařízeních. Šablona práce určuje, jak se práce provádí pro každý skladový proces, a směrnice o umístění určuje umístění pro výdej a vkládání pro pohyb zásob. Další informace naleznete v tématu [Řízení práce ve skladu pomocí šablon práce a směrnic skladového místa](control-warehouse-location-directives.md).

> [!NOTE]
> Ve výchozím nastavení jsou vlny zpracovávány v dávkovém režimu.

Během zpracování vlny systém obvykle vytvoří nový náklad pro každou dodávku, ke které není přiřazen žádný náklad. Pokud chcete, aby systém místo toho přiřazoval nepřiřazené zásilky ke stávajícím nákladům, můžete použít pokročilé funkce budování vlnového zatížení. Další informace viz [Rozšířené sestavení nákladu během vlny](advanced-load-building-during-wave.md).

Na stránkách **Prodejní objednávky** a **Přenos objednávek** můžete zkontrolovat entity, které jsou vytvořeny pro řádky objednávek během procesu vydání do skladu.

- Stránka **Prodejní objednávky**:

    - Na záložce s náhledem **Řádky prodejní objednávky** vyberte **Sklad** a poté v nabídce vyberte **Podrobnosti o zásilce** k otevření souvisejících zásilek, **Načíst podrobnosti** k otevření souvisejících zatížení nebo **Podrobnosti o práci** k otevření souvisejících detailů práce.
    - Na záložce s náhledem **Podrobnosti řádku** vyberte kartu **Vytížení** pro kontrolu souvisejících vytížení.

- Stránka **Převodní příkazy**:

    - V podokně akcí na kartě **Expedice** vyberte kartu **Podrobnosti o zásilce** k otevření souvisejících zásilek nebo **Načíst podrobnosti** k otevření souvisejících zatížení.
    - Na záložce s náhledem **Přenos řádků objednávky** vyberte **Podrobnosti o práci** k otevření souvisejících detailů práce.

Na závěr, když je objednávka uvolněna do skladu, nejvíce automatizovaný tok funguje následujícím způsobem:

1. Systém vytvoří zásilku pro objednávku a vlnu.
1. Vlna je zpracována.
1. Systém vytvoří ID zátěže a práce.

V závislosti na šablonách vln, pracovních šablonách a nastavení směrnic umístění mohou některé kroky v tomto toku začít být manuálními. Celkový tok však zůstává stejný.

Máte několik možností, jak uvolnit objednávku do skladu. Operaci můžete provést ručně nebo můžete nastavit dávkovou úlohu. Zbývající části tohoto tématu podrobně přezkoumají různé způsoby, jak můžete provést operaci uvolnění do skladu.

## <a name="manual-release-to-the-warehouse-from-the-sales-orders-and-transfer-orders-pages"></a>Ruční uvolnění do skladu ze stránek Prodejní objednávky a Přenos objednávek

Objednávku můžete uvolnit do skladu přímo ze stránky **Prodejní objednávky** nebo stránky **Objednávky přenosu** výběrem možnosti **Uvolnit do skladu**.

- Na stránce **Prodejní objednávky** je tlačítko **Sklad** v podokně akcí.
- Na stránce **Objednávky převodu** je tlačítko na kartě **Expedovat** v podokně akcí.

Ze stránky **Prodejní objednávky** můžete uvolnit několik prodejních objednávek současně.

## <a name="manual-release-to-the-warehouse-from-the-release-to-warehouse-pages"></a>Ruční uvolnění do skladu ze stránek Uvolnit do skladu

Systém aktuálně poskytuje tři stránky, kde můžete zkontrolovat řádky pro více objednávek a uvolnit je do skladu:

- **Uvolnit do skladu** (**Správa skladu \> Uvolnit do skladu \> Uvolnit do skladu**) - Tato stránka vám umožňuje pracovat jak s prodejními objednávkami, tak s převodními objednávkami. Poskytuje však pomalejší výkon než ostatní dvě stránky. Tato stránka bude brzy zastaralá.
- **Uvolnit prodejní objednávky** (**Správa skladu \> Uvolnit do skladu \> Uvolnit prodejní objednávky do skladu**) - Tato stránka vám umožňuje pracovat jen s prodejními objednávkami. Poskytuje však lepší výkon než stránka **Uvolnit do skladu**.
- **Uvolnit objednávky převodu do skladu** (**Správa skladu \> Uvolnit do skladu \> Uvolnit objednávky převodu do skladu**) - Tato stránka vám umožňuje pracovat jen s objednávkami převodu. Poskytuje však lepší výkon než stránka **Uvolnit do skladu**.

Všechny tři stránky poskytují podobnou funkci, jak je popsáno ve zbytku této části. Všechny vám umožňují vybrat řádky objednávek nebo celé objednávky a poté je uvolnit do skladu.

Každá ze stránek se skládá z horní části, kde můžete vybrat řádky objednávky, a ze spodní části, kde můžete zahájit proces uvolnění do skladu. K vyhledání řádků prodejní objednávky, které chcete uvolnit, můžete použít filtry v horní části. Stránka **Uvolnit do skladu** poskytuje v horní části samostatnou kartu pro prodejní objednávky a objednávky převodu, zatímco každá z dalších dvou stránek zobrazuje pouze jeden typ objednávky.

Panel nástrojů v horní části obsahuje následující tlačítka, pomocí kterých můžete vybrat řádky objednávek, které chcete uvolnit do skladu:

- **Přidat** - V horní části vyberte jeden nebo více řádků objednávky a poté vyberte toto tlačítko pro tyto řádky v dolní části.
- **Přidat vše** - Přidejte všechny řádky z horní části do spodní části.
- **Přidat objednávku** - Vyberte objednávku a poté pomocí tohoto tlačítka přidejte do dolní části všechny řádky z této objednávky.

Jakmile přidáte řádky do spodní části, označte každý řádek, který chcete uvolnit. Poté vyberte **Uvolnit do skladu** na panelu nástrojů pro uvolnění těchto řádků do skladu.

## <a name="manual-release-to-the-warehouse-from-the-load-planning-workbench-page"></a>Ruční uvolnění do skladu ze stránky načíst workbench plánování

Objednávky můžete také uvolnit do skladu ručně pomocí stránky **Workbench pro plánování vytížení**. Tato stránka vám umožňuje uspořádat řádky objednávek do vytížení a poté je uvolnit do skladu.

Pokud chcete otevřít stránku **Workbench plánování vytížení**, jděte na **Správa skladu \> Vytížení**. Můžete jej také otevřít ze stránky **Prodejní objednávky** a **Objednávky převodu**. V horní části stránky můžete vybrat řádky prodejní objednávky na kartě **Řádky prodeje** a řádky objednávky převodu na kartě **Řádky převodu** kartu a poté přidat tyto řádky do nového nebo stávajícího vytížení.

Karta **Nabídka a poptávka** v podokně akcí obsahuje následující tlačítka, která můžete použít k přidání řádků objednávky v horní části do vytížení:

- **Do nového vytížení** - V horní části vyberte jeden řádek objednávky a pak pomocí tohoto tlačítka vytvořte nové vytížení a přidejte do něho tyto řádky.
- **Do existujícího vytížení** - V horní části vyberte řádky objednávky a pak pomocí tohoto tlačítka přidejte tyto řádky do existujícího vytížení.
- **Celá objednávka do nového vytížení** - V horní části vyberte jeden řádek objednávky a pak do něho přidejte všechny řádky z těchto objednávek.
- **Celá objednávka do existujícího vytížení** - Vyberte objednávku a pak pomocí tohoto tlačítka přidejte všechny řádky z této objednávky do existujícího vytížení.

V dolní části si můžete prohlédnout vytvořená vytížení. Pokud chcete uvolnit vytížení do skladu, vyberte je a pak vyberte **Uvolnit \> Uvolnit do skladu** na panelu nástrojů. Pokud používáte automatické zpracování vln, protože vytížení jsou již přiřazena řádkům objednávky, systém po provedení operace uvolnění do skladu vytvoří ID zásilek a práce.

## <a name="automatic-release-to-the-warehouse"></a>Automatické uvolnění do skladu

Chcete -li automaticky uvolňovat objednávky do skladu, použijte úlohy **Automatické uvolňování prodejních objednávek** a **Automatické uvolňování převodních příkazů**.

Pro nastavení dávkové úlohy, která vydává prodejní objednávky, postupujte následovně.

1. Přejděte na **Řízení skladu \> Uvolnění do skladu \> Automatické uvolnění prodejních objednávek**.
1. V dialogovém okně **Automatické uvolnění prodejních objednávek** na záložce s náhledem **Parametry** nastavte následující pole:

    - **Množství k uvolnění** - vyberte, zda má být v dávce uvolněné celé množství nebo jen fyzicky rezervované množství.
    - **Povolit uvolnění částečně uvolněných objednávek** - Určete, zda má být zbývající množství pro částečně uvolněné objednávky uvolněno do skladu.
    - **Ponechat rezervace při selhání vydání** - Určete, zda by množství, která byla automaticky vyhrazena pro prodejní objednávku, zůstala vyhrazena, pokud proces uvolnění do skladu selže.
    - **Seskupit vydání podle zákazníka** – Tato možnost určuje, zda má systém zpracovávat vydání do skladových operací zvlášť pro každého zákazníka, nebo zda má uvolňovat všechny prodejní objednávky najednou. Když je tato možnost nastavena na *Ano*, systém shromáždí všechny řádky prodejní objednávky pro vybraného zákazníka, uvolní tyto objednávky do skladu a poté zpracuje dalšího zákazníka. Když je tato možnost nastavena na *Ne*, systém uvolní všechny dostupné řádky prodejní objednávky v jednom vydání do operace skladu. Povolení této možnosti může pomoci zvýšit výkon a odolnost procesu uvolnění do skladu. Při použití této možnosti spolu se šablonami vln, které jsou nakonfigurovány na „Zpracování vlny při vydání do skladu“, však musíte být opatrní, protože tato kombinace může generovat mnoho vln pro jednoho zákazníka, každou s prací generovanou pouze pro tohoto zákazníka. Pokud chcete generovat práci, která kombinuje zásilky pro více zákazníků, měli byste buď vypnout možnost *Seskupit vydání podle zákazníka*, nebo nakonfigurovat šablony vln pro použití odloženého zpracování.
    - **Uzamčené zpracování objednávky** - Vyberte, jak má systém zpracovávat prodejní objednávky, které jsou aktuálně zamčené, protože je upravují jiní uživatelé nebo procesy:

        - *Počkat, až se odemknou objednávky* - Systém by měl počkat, až se objednávky odemknou, než je uvolní do skladu. V tomto případě může proces uvolnění do skladu trvat déle.
        - *Přeskočit zamčené objednávky* - Systém by měl přeskakovat zamčené objednávky.

    - **Platné typy objednávek** - Vyberte typy prodejních objednávek, které chcete zahrnout do dávky.
    - **Typ úvěrového limitu** - Vyberte, zda mají být během procesu uvolnění do skladu prováděny kontroly úvěrových limitů, a pokud mají být kontroly prováděny, informace o transakcích, které do nich mají být zahrnuty.

1. Chcete -li určit, které objednávky by měly být zpracovány, na záložce s náhledem **Záznamy k zahrnutí** vyberte **Filtr**. Zobrazí se standardní dialogové okno dotazu, kde můžete definovat kritéria výběru, kritéria řazení a spojení. Pole fungují stejně jako u jiných typů dotazů v Microsoft Dynamics 365 Supply Chain Management.
1. Na záložce s náhledem **Spustit na pozadí** zvolte, zda by úloha měla běžet v dávkovém režimu a/nebo nastavit opakující se rozvrh. Pole fungují stejně jako u jiných typů [prací na pozadí](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) v Supply Chain Management.
1. Výběrem **OK** použijte vaše nastavení a spusťte proces vydání do skladu.

Pro nastavení dávkové úlohy, která vydává převodní objednávky, postupujte následovně.

1. Přejděte na **Řízení skladu \> Uvolnit do skladu \> Automaticky uvolnit převodní příkazy**.
1. V dialogovém okně **Automatické uvolnění převodní objednávek** na záložce s náhledem **Parametry** nastavte následující pole:

    - **Množství k uvolnění** - vyberte, zda má být v dávce uvolněné celé množství nebo jen fyzicky rezervované množství.
    - **Povolit uvolnění částečně uvolněných objednávek** - Určete, zda má být zbývající množství pro částečně uvolněné objednávky uvolněno do skladu.
    - **Skupinová vydání podle cílového skladu** - Určete, zda má systém uvolňovat všechny převodní příkazy současně, nebo zda má seskupovat řádky převodních příkazů podle cílového skladu a poté uvolnit každou skupinu do skladu samostatně.

1. Chcete -li určit, které objednávky by měly být zpracovány, na záložce s náhledem **Záznamy k zahrnutí** vyberte **Filtr**. Zobrazí se standardní dialogové okno dotazu, kde můžete definovat kritéria výběru, kritéria řazení a spojení. Pole fungují stejně jako u jiných typů dotazů v Supply Chain Management.
1. Na záložce s náhledem **Spustit na pozadí** zvolte, zda by úloha měla běžet v dávkovém režimu a/nebo nastavit rozvrh opakování. Pole fungují stejně jako u jiných typů [prací na pozadí](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) v Supply Chain Management.
1. Výběrem **OK** použijte vaše nastavení a spusťte proces vydání do skladu.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
