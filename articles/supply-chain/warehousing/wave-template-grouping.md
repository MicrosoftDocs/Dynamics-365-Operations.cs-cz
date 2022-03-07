---
title: Seskupení šablon vlny
description: Seskupení šablon vlny umožňuje systému použít nastavení šablon vlny k určení postupu dělení uvolněných řádků a jejich přiřazování k novým nebo existujícím vlnám na základě definovaných kritérií. Tato funkce může být užitečná ve skladech, kde se tvoří vlny na základě konkrétních kritérií, ale kde manažeři dávají přednost automatické tvorbě vln místo ručního postupu.
author: Mirzaab
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWaveTableListPage, WHSWaveTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: b265c0d5cb43e151386fe90e3a3dea414ec0aca6
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/29/2021
ms.locfileid: "7579897"
---
# <a name="wave-template-grouping"></a>Seskupení šablon vlny

[!include [banner](../includes/banner.md)]

Seskupení šablon vlny umožňuje systému použít nastavení [šablon vlny](tasks/configure-wave-processing.md) k určení postupu dělení uvolněných řádků a jejich přiřazování k novým nebo existujícím vlnám na základě definovaných kritérií. Tato funkce může být užitečná ve skladech, kde se tvoří vlny na základě konkrétních kritérií, ale kde manažeři dávají přednost automatické tvorbě vln místo ručního postupu. Umožňuje, aby byly v systému přidávány nově uvolněné dodávky do první vlny, u níž se určí shoda s příslušnou hodnotou v poli seskupení. Pokud shoda není zjištěna, vytvoří systém pro novou dodávku novou vlnu.

> [!IMPORTANT]
> Seskupení šablon vlny není podporováno u prací typu *výdej surovin pro výrobu* nebo *kanban – výdej*. Je to proto, že seskupování podle vln je založeno na dodávkách, ale tyto typy prací nepoužívají dodávky.

## <a name="turn-on-the-wave-template-grouping-feature"></a>Zapnutí funkce seskupení šablon vlny

Než můžete použít funkci *Seskupení šablon vlny*, musíte ji v systému zapnout. Správci mohou pomocí nastavení [správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) zkontrolovat stav funkce a zapnout ji, je-li to potřeba. V pracovním prostoru **Správa funkcí** je tato funkce uvedena následovně:

- **Modul:** *Řízení skladu*
- **Název funkce** *Seskupení šablon vlny*

## <a name="set-a-wave-template-to-use-wave-template-grouping"></a><a name="set-up-template"></a>Nastavení šablony vlny k použití pro seskupení šablon vlny

Chcete-li zpřístupnit seskupení šablon vlny, nastavte [šablonu vlny](tasks/configure-wave-processing.md) v souladu s pokyny níže.

1. Přejděte na **Řízení skladu \> Nastavení \> Vlny \> Šablony vlny**.
1. V levém podokně vyberte šablonu vlny, kterou chcete nastavovat. Pokud se chystáte využít scénář uvedený dále v tomto tématu s využitím ukázkových dat, vyberte šablonu **Výchozí dodávka 62**.
1. Vyberte možnost **Upravit**, tím přepnete stránku do režimu úprav.
1. Na záložce s náhledem **Obecné** nastavte následující hodnoty:

    - **Automatizovat tvorbu vln:** *Ano*
    - **Přiřadit k otevřeným vlnám:** *Ano*
    - **Zpracovat vlnu při uvolnění do skladu:** *Ne*

1. V podokně akcí zvolte **Upravit dotaz** a otevřete dialogové okno dotazů.
1. V dialogovém okně dotazů zkontrolujte na kartě **Třídění** kritéria třídění a ujistěte se, že existuje pravidlo zahrnující pole, jež chcete použít k seskupení vln.

    Pokud se chystáte použít scénář s ukázkovými daty, přidejte řádek s následujícími hodnotami:

    - **Tabulka:** *Dodávky*
    - **Odvozená tabulka:** *Dodávky*
    - **Pole:** *Služba dopravce*

        > [!NOTE]
        > Po výběru této hodnoty se vám může zobrazit následující zpráva: „Služba dopravce není indexové pole. Chcete k němu přidat třídění?“ Třídění přidáte kliknutím na **Ano**.

    - **Směr hledání:** *Vzestupně*

1. Vyberte **OK**, uložte změny a zavřete okno dotazů.
1. V podokně Akce vyberte možnost **Seskupení šablon vlny**.
1. Na stránce **Seskupení šablon vlny** zaškrtněte políčko **Seskupit podle** u každého řádku, který chcete použít k seskupení řádků objednávky do vln, jak je třeba. Pokud se chystáte použít scénář s ukázkovými daty, zaškrtněte políčko **Seskupit podle** u řádku *Služba dopravce*.
1. Zvolte **Uložit**.
1. Zavřete stránku **Seskupení šablon vlny**.
1. Klepnutím na tlačítko **Uložit** uložte šablonu.

## <a name="scenario"></a>Scénář

Tato část obsahuje skript, pomocí kterého můžete zjistit, co tato funkce provádí a jak s ní lze pracovat.

### <a name="make-sample-data-available"></a>Příprava ukázkových dat

Chcete-li s tímto scénářem pracovat pomocí zde specifikovaných ukázkových záznamů a hodnot, musíte používat systém, ve kterém jsou nainstalována standardní [ukázková data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md). Kromě toho musíte dříve, než začnete, také vybrat právnickou osobu **USMF**.

Tento scénář můžete také použít jako vodítko pro použití této funkce při práci na produkčním systému. V takovém případě však musíte nahradit uvedené hodnoty vlastními hodnotami. Také možná budete postrádat některé typy požadovaných záznamů, jež jsou součástí standardních ukázkových dat.

### <a name="scenario-wave-template-grouping"></a>Scénář: Seskupení šablon vlny

Tento scénář ukazuje, jak pomocí seskupení šablon vlny automaticky vytvářet více vln na základě kritérií seskupení definovaných v šabloně vlny. V tomto scénáři je šablona vlny nastavena v systému tak, aby vytvořila jednu vlnu pro každou službu dopravce.

Než začnete, připravte si šablonu vlny postupem popsaným v tématu v části [Nastavení šablony vlny k použití pro seskupení šablon vlny](#set-up-template) výše. Pokud budete využívat tento scénář s ukázkovými daty, je třeba použít hodnoty z ukázkových dat, jak se v proceduře navrhuje. Toto nastavení seskupí vaše vlny podle služby dopravce, jež je nastavena pro každou prodejní objednávku.

#### <a name="create-sales-order-1"></a>Vytvoření prodejní objednávky 1

1. Přejděte na **Prodej a marketing \> Prodejní objednávky \> Všechny prodejní objednávky**.
1. Klepnutím na možnost **Nová** vytvořte novou prodejní objednávku.
1. V dialogovém okně **Vytvoření prodejní objednávky** nastavte následující hodnoty:

    - Na záložce s náhledem **Odběratel** zadejte do pole **Účet odběratele** hodnotu *US-004*.
    - Na záložce s náhledem **Obecné** zadejte do pole **Sklad** hodnotu *62*.

1. Stisknutím **OK** vytvoříte prodejní objednávku a zavřete dialogové okno **Vytvoření nákupní objednávky**.
1. Nová prodejní objednávka se otevře v zobrazení **Řádky**. Poznamenejte si číslo prodejní objednávky.
1. Přepněte na zobrazení **Záhlaví**.
1. Na záložce s náhledem **Doručení** nastavte v sekci **Přeprava** následující hodnoty:

    - **Dopravce dodávky:** *Letecká přeprava*
    - **Služba dopravce:** *Air*

1. Přepněte znovu do zobrazení **Řádky**.
1. V oddílu **Řádky prodejní objednávky** přidejte řádek mřížky výběrem položky **Přidat řádek**.
1. Na novém řádku nastavte následující hodnoty:

    - **Číslo položky:** *A0002*
    - **Množství:** *2*

1. Vyberte nový řádek objednávky a poté v nabídce **Zásoby** nad mřížkou vyberte možnost **Rezervace**.
1. Na stránce **Rezervace** v podokně Akce klikněte na **Rezervovat šarži**. Ve skladu se provede rezervace celého množství vybraného řádku.
1. Zavřete stránku **Rezervace** a vraťte se k prodejní objednávce.
1. V podokně akcí na kartě **Sklad** ve skupině **Akce** vyberte možnost **Uvolnit do skladu.**
1. Obdržíte informační zprávu, v níž bude zobrazena dodávka a vlna pro danou objednávku. Poznamenejte si čísla ID vlny a dodávky.

#### <a name="view-the-wave-that-was-created-from-sales-order-1"></a>Zobrazení vlny, která byla vytvořena z prodejní objednávky 1

1. Přejděte na **Řízení skladu \> Výstupní vlny \> Vlny dodávek \> Všechny vlny**.
1. Vyberte ID vlny, která byla vytvořena z prodejní objednávky.
1. Kliknutím na odkaz ID vlny otevřete stránku podrobností vlny.
1. Všimněte si, že dodávka byla přidána na záložku s náhledem **Řádky vlny**.

#### <a name="create-sales-order-2"></a>Vytvoření prodejní objednávky 2

1. Přejděte na **Prodej a marketing \> Prodejní objednávky \> Všechny prodejní objednávky**.
1. Klepnutím na možnost **Nová** vytvořte novou prodejní objednávku.
1. V dialogovém okně **Vytvoření prodejní objednávky** nastavte následující hodnoty:

    - Na záložce s náhledem **Odběratel** zadejte do pole **Účet odběratele** hodnotu *US-005*.
    - Na záložce s náhledem **Obecné** zadejte do pole **Sklad** hodnotu *62*.

1. Stisknutím **OK** vytvoříte prodejní objednávku a zavřete dialogové okno **Vytvoření nákupní objednávky**.
1. Nová prodejní objednávka se otevře v zobrazení **Řádky**. Poznamenejte si číslo prodejní objednávky.
1. Přepněte na zobrazení **Záhlaví**.
1. Na záložce s náhledem **Doručení** nastavte v sekci **Přeprava** následující hodnoty:

    - **Dopravce dodávky:** *Flower moving*
    - **Služba dopravce:** *Std*

1. Přepněte znovu do zobrazení **Řádky**.
1. V oddílu **Řádky prodejní objednávky** přidejte řádek mřížky výběrem položky **Přidat řádek**.
1. Na novém řádku nastavte následující hodnoty:

    - **Číslo položky:** *A0001*
    - **Množství:** *1*

1. Vyberte nový řádek objednávky a poté v nabídce **Zásoby** nad mřížkou vyberte možnost **Rezervace**.
1. Na stránce **Rezervace** v podokně Akce klikněte na **Rezervovat šarži**. Ve skladu se provede rezervace celého množství vybraného řádku.
1. Zavřete stránku **Rezervace** a vraťte se k prodejní objednávce.
1. V podokně akcí na kartě **Sklad** ve skupině **Akce** vyberte možnost **Uvolnit do skladu.**
1. Obdržíte informační zprávu, v níž bude zobrazena dodávka a vlna pro danou objednávku. Poznamenejte si čísla ID vlny a dodávky. Všimněte si, že ID vlny se liší od ID vlny první prodejní objednávky.

#### <a name="view-the-wave-that-was-created-from-sales-order-2"></a>Zobrazení vlny, která byla vytvořena z prodejní objednávky 2

1. Přejděte na **Řízení skladu \> Výstupní vlny \> Vlny dodávek \> Všechny vlny**.
1. Vyberte ID vlny, která byla vytvořena z druhé prodejní objednávky.
1. Kliknutím na odkaz ID vlny otevřete stránku podrobností vlny.
1. Všimněte si, že dodávka byla přidána na záložku s náhledem **Řádky vlny**.

Pro tuto dodávku byla vytvořena nová vlna, protože používá jinou službu dopravce než první prodejní objednávka.

#### <a name="create-sales-order-3"></a>Vytvoření prodejní objednávky 3

1. Přejděte na **Prodej a marketing \> Prodejní objednávky \> Všechny prodejní objednávky**.
1. Klepnutím na možnost **Nová** vytvořte novou prodejní objednávku.
1. V dialogovém okně **Vytvoření prodejní objednávky** nastavte následující hodnoty:

    - Na záložce s náhledem **Odběratel** zadejte do pole **Účet odběratele** hodnotu *US-006*.
    - Na záložce s náhledem **Obecné** zadejte do pole **Sklad** hodnotu *62*.

1. Stisknutím **OK** vytvoříte prodejní objednávku a zavřete dialogové okno **Vytvoření nákupní objednávky**.
1. Nová prodejní objednávka se otevře v zobrazení **Řádky**. Poznamenejte si číslo prodejní objednávky.
1. Přepněte na zobrazení **Záhlaví**.
1. Na záložce s náhledem **Doručení** nastavte v sekci **Přeprava** následující hodnoty:

    - **Dopravce dodávky:** *Letecká přeprava*
    - **Služba dopravce:** *Air*

1. Přepněte znovu do zobrazení **Řádky**.
1. V oddílu **Řádky prodejní objednávky** přidejte řádek mřížky výběrem položky **Přidat řádek**.
1. Na novém řádku nastavte následující hodnoty:

    - **Číslo položky:** *A0001*
    - **Množství:** *1*

1. Vyberte nový řádek objednávky a poté v nabídce **Zásoby** nad mřížkou vyberte možnost **Rezervace**.
1. Na stránce **Rezervace** v podokně Akce klikněte na **Rezervovat šarži**. Ve skladu se provede rezervace celého množství vybraného řádku.
1. Zavřete stránku **Rezervace** a vraťte se k prodejní objednávce.
1. V podokně akcí na kartě **Sklad** ve skupině **Akce** vyberte možnost **Uvolnit do skladu.**
1. Obdržíte informační zprávu, v níž bude zobrazena dodávka a vlna pro danou objednávku. Poznamenejte si čísla ID vlny a dodávky. Dodávka byla přiřazena ke stávající vlně z první prodejní objednávky.

#### <a name="view-the-wave-for-sales-orders-1-and-3"></a>Zobrazení vlny pro prodejní objednávky 1 a 3

1. Přejděte na **Řízení skladu \> Výstupní vlny \> Vlny dodávek \> Všechny vlny**.
1. Vyberte ID vlny, která byla vytvořena ze třetí prodejní objednávky.
1. Kliknutím na odkaz ID vlny otevřete stránku podrobností vlny.
1. Všimněte si, že dodávka byla přidána na záložku s náhledem **Řádky vlny** spolu s dodávkou za první prodejní objednávku.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]