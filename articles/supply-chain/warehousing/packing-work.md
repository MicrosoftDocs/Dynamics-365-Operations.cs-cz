---
title: Balicí práce pro balení odchozích kontejnerů a zpracování zásilek
description: Tento článek popisuje typ pracovního příkazu „Balení“, který spravuje práci pro balení kontejnerů a podporuje částečné dodávky zabalených kontejnerů souvisejících s náklady, kde skladové položky zůstávají rozbalené.
author: perlynne
ms.date: 7/13/2022
ms.topic: article
ms.search.form: WHSPackingWorkLocationSetup, WHSPack, WHSContainerTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2022-08-01
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: 34a7087df7e7768d0012ea4f534aa109654af8fa
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/02/2022
ms.locfileid: "9220525"
---
# <a name="packing-work-for-packing-outbound-containers-and-processing-shipments"></a>Balicí práce pro balení odchozích kontejnerů a zpracování zásilek

[!include [banner](../../includes/banner.md)]

Tento článek popisuje typ pracovního příkazu *Balení*, který spravuje práci pro balení kontejnerů a podporuje částečné dodávky zabalených kontejnerů souvisejících s náklady, kde skladové položky zůstávají rozbalené. Balicí práce vám umožní používat funkci [potvrdit a přenést](confirm-and-transfer.md) pro potvrzení odchozích zásilek, které jsou spojeny s kontejnery.

Balicí práce se automaticky vytvoří, když jsou zásoby, které souvisí s prací se zdrojovým dokumentem, umístěny do umístění typu *Místo balení*. Práce se skládá ze dvou řádků, jeden pro *Vychystávání* a jeden pro *Vložení*, a je automaticky udržována jako součást procesu uzavření / znovu otevření kontejneru.

Další informace o tom, jak nastavit a používat proces balení kontejnerů, viz [Balení kontejnery pro přepravu](packing-containers.md).

## <a name="turn-on-the-feature"></a>Zapnutí funkce

Pokud váš systém ještě neobsahuje funkce popsané v tomto článku, přejděte na stránku [Správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) a zapínejte následující funkce v následujícím pořadí. Obě funkce jsou součástí modulu **Správa skladu**.

1. *Potvrdit a převést*
1. *Práce balení pro balicí stanice*

## <a name="set-up-a-location-for-packing-work"></a>Nastavení umístění pro balicí práci

Pomocí následujícího postupu nastavte místa balení. Pro každé umístění můžete vybrat, zda systém automaticky vytvoří balicí práce.

1. Přejděte do nabídky **Řízení skladu \> Nastavení \> Balení \> Nastavení balicí stanice**.
1. V podokně Akce vyberte možnost **Nový**. Tím se přidá záznam nastavení balicí stanice.
1. V novém záznamu nastavte následující pole:

    - **Sklad** – Vyberte nebo zadejte sklad, kde se nachází místo balení.
    - **Místo** – Zadejte nebo vyberte místo balení. Toto místo musí být přiřazeno k profilu místa, který používá typ místa, který je nakonfigurován jako typ místa balení pro vaši společnost na stránce **Parametry řízení skladu**. Více informací viz [Balení kontejnerů pro přepravu](packing-containers.md).
    - **Vytvoření balicí práce** – Zaškrtněte toto políčko, chcete-li vytvořit balicí práce pokaždé, když jsou položky doručeny na místo balení. Práce bude obsahovat odkazy na související řádky nákladu, aby bylo možné zabalit a odeslat částečné náklady.

## <a name="example-scenario"></a>Příklad

Tento příklad ukazuje, jak zpracovat tok odchozí prodejní objednávky zabalením kontejneru a odesláním částečného nákladu.

### <a name="make-sample-data-available"></a>Příprava ukázkových dat

Chcete-li s tímto scénářem pracovat pomocí zde specifikovaných ukázkových záznamů a hodnot, musíte používat systém, ve kterém jsou nainstalována standardní [ukázková data](../../fin-ops-core/fin-ops/get-started/demo-data.md). Kromě toho musíte dříve, než začnete, také vybrat právnickou osobu **USMF**.

Tento scénář můžete také použít jako vodítko pro použití této funkce v produkčním systému. V takovém případě však musíte každé vlastní nastavení, které je zde popsáno, nahradit vlastními hodnotami.

### <a name="configure-packing-work-for-warehouse-packing-location"></a>Konfigurace balicí práce pro místo balení ve skladu

Chcete-li začít, musíte nakonfigurovat pracovní proces *Balení* pro konkrétní sklad a místo.

1. Přejděte do nabídky **Řízení skladu \> Nastavení \> Balení \> Nastavení balicí stanice**.
1. V podokně Akce volbou **Nový** přidejte záznam nastavení.
1. V novém záznamu nastavte následující hodnoty:

    - **Sklad:** *62*
    - **Místo:** *balení*
    - **Vytvořit práci balení:** *Ano*

1. Zavřete stránku **Nastavení balicí stanice**.

### <a name="create-a-load-template-that-allows-partial-shipping"></a>Vytvoření šablony nákladu, která umožňuje částečnou expedici

Chcete-li povolit doručení nákladu prostřednictvím více zásilek, musíte ho přiřadit k šabloně nákladu, která umožňuje částečnou přepravu. Při vytváření požadované šablony postupujte podle těchto kroků.

1. Přejděte do **Řízení skladu \> Nastavení \> Náklad \> Šablony nákladů**.
1. V podokně Akce volbou **Nový** přidejte záznam nastavení.
1. V novém záznamu nastavte následující hodnoty:

    - **ID šablony nákladu:** *Částečné*
    - **Povolit rozdělení vytížení během potvrzení expedice:** *Ano*

1. Zavřete stránku **Šablony nákladu**.

Další informace viz [Potvrdit a převést](Confirm-and-transfer.md).

### <a name="process-a-sales-order"></a>Zpracování prodejní objednávky

Chcete-li zpracovat prodejní objednávku a částečně ji expedovat, postupujte podle těchto kroků.

1. Proveďte [příkladový scénář](packing-containers.md#scenario), který je uveden v části [Balení kontejnerů pro přepravu](packing-containers.md). Během tohoto scénáře vytvoříte prodejní objednávku pro dva kusy jedné položky. Do kontejneru pak zabalíte pouze jeden z kusů a kontejner uzavřete. Měli byste si poznamenat ID zásilky, které vytvoříte, jak je uvedeno ve scénáři.
1. Přejděte do **Řízení skladu \> Práce\> Všechny práce**.
1. V oblasti filtru vyberte zaškrtávací políčko **Zobrazit uzavřenou práci**. Poté zadejte ID zásilky do pole **Filtr** a vyberte filtrování podle hodnoty **ID zásilky**. Nyní byste měli vidět tři pracovní záhlaví. Jedno je pro práci vychystávání prodejní objednávky a má stav *Uzavřeno*. Dvě jsou pro proces balení: jedno se vztahuje k uzavřenému kontejneru a má stav *Uzavřeno* a druhé souvisí s rozbalenou zbývající položkou a má stav *Otevřeno*.
1. Vyberte hodnotu **ID nákladu** pro kterékoli z pracovních záhlaví pro otevření stránky **Údaje nákladu** pro náklad.
1. Přepněte na zobrazení **Záhlaví**.
1. Na pevné záložce **Obecné** vyberte tlačítko **Upravit** pro pole **ID šablony nákladu**. Poté vyberte šablonu nákladu částečné expedice, kterou jste vytvořili pro tento scénář (*Částečná*).
1. V podokně akcí na kartě **Expedovat a přijmout** ve skupině **Potvrdit** vyberte **Odchozí zásilka**.
1. V dialogovém okně **Potvrzení expedice** vyberte možnost **Rozdělit množství na nový náklad**.
1. Vyberte **OK**.

Nyní jste odeslali jeden kontejner, který souvisí s původním nákladem, a systém vytvořil nový náklad pro zbývající položky, které musí být ještě zabaleny do kontejnerů.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
