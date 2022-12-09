---
title: Naplánujte tisk vlnových štítků během vlny
description: Tento článek popisuje, jak nastavit a používat funkce pro tisk štítků vln založených na úlohách.
author: perlynne
ms.date: 12/02/2022
ms.topic: article
ms.search.form: WHSPostMethod, WHSWavePostMethodTaskConfig, WHSWaveTemplateTable, WHSParameters, WHSWaveTableListPage, WHSWorkTableListPage, WHSWorkTable, BatchJobEnhanced, WHSPlannedWorkOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-09
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: e788e5a9206e46ada6490d4a0196c7ea8ca6af15
ms.sourcegitcommit: 04e42c495d018e457fb3b038cadc4fe75ecbba12
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/02/2022
ms.locfileid: "9822355"
---
# <a name="schedule-wave-label-printing-during-wave"></a>Naplánujte tisk vlnových štítků během vlny

[!include [banner](../../includes/banner.md)]

Použijte funkci *Tisk štítků vln na základě úkolů* jako součást vašeho procesu vln, který pomůže zlepšit efektivitu a umožní systému vytvářet štítky vln a pracovat v samostatných úkolech.

Proces konfigurace tisku štítků vln je složitý a spoléhá se na přesnou konfiguraci a kmenová data. Není neobvyklé, že generování záznamů štítků vln selhalo, a když k tomu dojde, vrátí se celé zpracování vln zpět. Funkce *Tisk štítků vln na základě úkolů* vám pomůže vyhnout se nutnosti znovu vytvářet práci a pracovní řádky pokaždé, když je popisek vlny vytištěn nesprávně.

Když používáte funkci *Tisk štítků vln na základě úkolů*, systém nejprve vytvoří práci a řádky práce. Poté vytvoří a vytiskne popisky vln. Nakonec, pokud jsou štítky vln správně vytvořeny, uvolní práci a vlnu pro výběr.

## <a name="turn-on-the-task-based-wave-label-printing-feature-in-feature-management"></a>Ve správě funkcí zapněte funkci tisku štítků vln na základě úkolů

Chcete-li používat funkce popsané v tomto článku, musí být pro váš systém zapnuty. Použijte pracovní prostor [Správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) a zapněte funkce v následujícím pořadí:

1. *Blokování práce v celé organizaci* - Tato funkce se vyžaduje pro ruční i automatickou konfiguraci plánovaného vytváření práce. (Od Supply Chain Management verze 10.0.21 je tato funkce povinná, takže je ve výchozím nastavení zapnutá a nelze ji znovu vypnout.)
1. *Tisk štítků vln na základě úlohy* - Tato funkce je nutná k rozdělení tisku štítků vln na samostatný rozsah transakcí.

## <a name="manually-enable-the-new-wave-step-method"></a>Ručně povolte novou metodu kroku vlny

Nejprve musíte vytvořit novou metodu kroku vlny a povolit ji pro paralelní asynchronní zpracování úloh.

1. Přejděte do **Řízení skladu \> Nastavení \> Vlny \> Metody zpracování vlny**.
1. V podokně Akce vyberte možnost **Obnovit metodu**. Všimněte si *waveLabelPrinting* je přidán do seznamu metod zpracování vln, které můžete použít ve svých šablonách přepravních vln.
1. Vyberte záznam, kde je pole **Název metody** nastaveno na *waveLabelPrinting* a poté v podokně akcí vyberte **Konfigurace úlohy**.
1. V podokně Akce vyberte možnost **Nový**. Tím se přidá řádek do mřížky. Poté pro nový řádek nastavte následující pole:

    - **Sklad** - Vyberte sklad, který budete používat k naplánování zpracování práce plánu. (Pokud používáte demo data pro účely testování, můžete vybrat sklad *24*.)
    - **Maximální počet dávkových úloh** - Určete maximální počet dávkových úloh. Ve většině případů by hodnota měla být od *8* do *16*. Doporučujeme však experimentovat, abyste našli optimální nastavení pro vaše scénáře.
    - **Skupina dávek pro zpracování ve vlnách** - Vyberte vyhrazenou skupinu dávek pro zpracování ve vlnách pro optimalizaci zpracování dávkové fronty.

Nyní můžete aktualizovat existující šablonu vln tak, aby používala metodu zpracování vln *Tisk štítků vln*. Alternativně můžete vytvořit novou vlnovou šablonu, která ji používá.

1. Přejděte na **Řízení skladu \> Nastavení \> Vlny \> Šablony vlny**.
1. V podokně akcí vyberte **Upravit**.
1. V podokně seznamu vyberte šablonu vlny, kterou chcete aktualizovat. (Pokud používáte demo data pro účely testování, můžete vybrat *Vychozí dodávka 24*.)
1. Na záložce s náhledem **Metody** ve sloupci **Zbývající metody** vyberte řádek, ve kterém je pole **Název** nastaveno na *waveLabelPrinting*.
1. Vyberte **přidat** (tlačítko se šipkou doprava) a přesuňte vybraný řádek do sloupce **Vybrané metody**.
1. Do pole **Kód kroku vlny** zadejte kód kroku vlny, který se použije pro připojení šablony vlny se šablonou štítku vlny.

## <a name="set-wave-task-processing-threshold-data"></a>Nastavení prahových dat zpracování vlnové úlohy

Systém vytvoří výchozí prahová data zpracování vlnových úloh při prvním spuštění vlnového procesu pomocí jakéhokoli zpracování založeného na úlohách. Tato data se používají k řízení, zda zpracování ve vlnách bude probíhat asynchronně a bude založeno na úkolech, což mu umožní paralelně vytvářet štítky vlny.

Výchozí data zpočátku používají prahovou hodnotu *1* pro minimální počet ID práce (`MinimumWorkThresholdForLabelPrinting`). Když tedy systém zpracovává vlnu, která má více než jeden ID práce, použije zpracování štítků vln na základě úkolů v samostatné transakci. Tato data můžete ručně vložit či aktualizovat do tabulky `WHSWaveTaskProcessingThresholdParameters` ve vašich testovacích prostředích. Cchete-li toto nastavení změnit v produkčním prostředí, musíte kontaktovat podporu Microsoftu a požádat o aktualizaci.

## <a name="changes-to-the-wave-processing-logic-when-task-based-wave-label-printing-is-used"></a>Změny logiky zpracování vln při použití tisku štítků vln na základě úlohy

Pokud zpracování štítku vlny překročí prahovou hodnotu pro zpracování vlnového úkolu, zahájí se zpracování na základě úkolu. V dalším zpracování vln, které odpovídá šabloně vlny, bude tisk štítků vln probíhat v samostatné transakci *ttsbegin*/*ttscommit* ihned po vytvoření práce. Pokud je uvolnění práce (odblokování) nakonfigurováno na šabloně vlny pro automatické spuštění, dojde k ní až po úspěšném dokončení procesu tisku štítků vln.

Pokud se generování štítku vlny nezdaří (například pokud selže převod množství práce na množství štítku vlny a vyvolá chybu), selže pouze příslušná transakce. Práce, která byla dříve vytvořena, zůstane zmrazená. Chcete-li opravit chyby a vytisknout štítky vln, postupujte takto.

1. Přejděte na **Řízení skladu \> Výstupní vlny \> Vlny dodávek \> Všechny vlny**.
1. Vyberte relevantní vlnu v mřížce.
1. V podokně akcí na kartě **Vlna** ve skupině **Tisk** zvolte **Vlnové štítky**.
1. Podle pokynů na obrazovce odešlete štítky k tisku.
1. V podokně akcí na kartě **Vlna** ve skupině **Vlna** vyberte **Uvolnit** pro ruční uvolnění práce pro vybranou vlnu.

## <a name="additional-resources"></a>Další prostředky

- [Tisk štítků vlny](configure-wave-label-printing.md)
- [Plánování vytváření práce během vlny](configure-wave-schedule-work-creation.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
