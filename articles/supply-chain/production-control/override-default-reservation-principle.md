---
title: Přepis výchozího principu rezervace pro materiály ve výrobě
description: Toto téma popisuje, jak nastavit výchozí zásadu rezervace pro každou skupinu modelů položek, takže pro každou položku, která je součástí vzorce kusovníku (BOM) nebo vzorce dávkové objednávky, lze automaticky použít různé zásady rezervace.
author: johanhoffmann
ms.date: 12/10/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventModelGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-12-10
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: a1b2dd204c9a507dba387b0295f3021253e02dc4
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5814795"
---
# <a name="override-the-default-reservation-principle-for-materials-in-production"></a>Přepis výchozího principu rezervace pro materiály ve výrobě

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

Funkce *Přepsat výchozí produkční rezervaci* umožňuje nastavit výchozí princip rezervace pro každou skupinu modelů položek. Proto lze pro každou položku, která je součástí vzorce kusovníku (BOM) nebo vzorce dávkové objednávky, automaticky použít různé zásady rezervace. Můžete si vybrat, zda má každá skupina modelů položek přepsat výchozí princip rezervace nastavený pro objednávku a jaký princip rezervace by měl být použit místo toho (*ruční*, *odhad*, *plánování*, *uvolnění* nebo *Start*).

Když vytvoříte novou výrobní zakázku nebo dávkovou objednávku, budete vyzváni k výběru principu rezervace, který by měl být použit pro danou objednávku a všechny její řádky kusovníku nebo řádky vzorce. Když je použita funkce *Přepsat výchozí rezervaci výroby*, některé nebo všechny řádky kusovníku nebo vzorce mohou tento princip rezervace přepsat a místo toho použít princip rezervace, který je nastaven pro příslušnou skupinu modelů položek.

Například pokud máte suroviny nebo přísady, které vyžadují výběr, kusovník nebo řádky vzorců, které jsou vytvořeny pro tyto produkty, vyžadují fyzickou rezervaci, protože fyzická rezervace je předpokladem pro generování skladové práce. Obvykle, pokud chcete, aby k rezervaci došlo automaticky, vyberete jeden z následujících principů rezervace: *odhad*, *plánování*, *uvolnění* nebo *Start*. Na druhou stranu, pokud máte materiály nebo přísady, které nevyžadují výběr, protože se spotřebovávají přímo z místa, obvykle vyberete *ruční* princip rezervace, který neprovádí žádné fyzické rezervace ani nevytváří žádnou práci s výběrem.

## <a name="turn-on-the-feature"></a>Zapnutí funkce

Než můžete použít tuto funkci, musíte ji zapnout ve svém systému. Správci mohou pomocí nastavení [správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) zkontrolovat stav funkce a zapnout ji. V pracovním prostoru **Správa funkcí** je tato funkce uvedena následovně:

- **Modul:** *Řízení výroby*
- **Název funkce:** *(Preview) Přepsat výchozí produkční rezervaci*

## <a name="assign-a-production-reservation-policy-to-an-item-model-group"></a>Přiřazení zásady rezervace výroby ke skupině modelů zboží

1. Jděte na **Cost Management \> Nastavení účetních zásad skladů \> Skupiny modelu položky**.
1. Vytvořte nebo vyberte skupinu modelů zboží.
1. Na kartě s náhledem **Zásady zásob** zaškrtněte políčko **Přepsat rezervaci výroby zboží**.
1. V poli **Rezervace** vyberte zásadu rezervace pro položky, které patří do vybrané skupiny modelů. (Mezi tyto položky patří položky, které jsou na kusovníku nebo vzorci.)

    - **Ruční** - Položky ve skupině modelů nebudou automaticky fyzicky vyhrazeny pro produkci. Stále je však možné je podle potřeby ručně rezervovat.
    - **Odhad** - Položky ve skupině modelů budou fyzicky rezervovány během odhadu výrobního příkazu.
    - **Plánování** - Položky ve skupině modelů budou fyzicky rezervovány během plánování výrobního příkazu.
    - **Vydání** - Položky ve skupině modelů budou fyzicky rezervovány během vydání výrobního příkazu.
    - **Start** - Položky ve skupině modelů budou fyzicky rezervovány na začátku výrobního příkazu.

## <a name="example-using-reservation-principles-in-a-bulkpack-scenario"></a>Příklad: Použití principů rezervace ve scénáři hromadného balení

Sypký mazací materiál se vyrábí v 1000litrovém mixéru. Jakmile je sypký materiál připraven, odčerpá se na několik čerpacích stanic, kde se plní lahve různých velikostí. Po dokončení plnění jsou lahve zabaleny do krabic. Tyto krabice se pak balí na palety.

V tomto scénáři je vytvořena dávková objednávka na výrobu 1 000 litrů sypkého materiálu. (Tato objednávka je hromadná objednávka.) Když je tato dávková objednávka dokončena, nahlásí se jako dokončená do místa vstupu materiálu čerpacích stanic. Poté se vytvoří dávková objednávka k naplnění a zabalení každé velikosti lahve. (Tyto objednávky jsou objednávky balení.) Objednávky balení mají vzorec, který se skládá z sypkého materiálu, prázdné láhve, štítku a dalších balicích materiálů. Vzhledem k tomu, že sypký materiál proudí přímo z míchací nádrže do čerpacích stanic, není k vyzvednutí této přísady zapotřebí žádné práce ve skladu a sypký materiál se spotřebovává přímo ze vstupního místa. Proto je princip rezervace nastaven na *ruční*. Ostatní materiály se do čerpací stanice přichystají vychystávací prací. Proto je u těchto linek nastaven princip rezervace *vydání*, například k tomu, aby rezervace proběhla automaticky při uvolnění objednávky balíčku.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]