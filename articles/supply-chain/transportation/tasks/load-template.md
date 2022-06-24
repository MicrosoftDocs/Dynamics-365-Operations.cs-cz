---
title: Šablony vytížení
description: Tento článek popisuje způsob nastavení šablony nákladů a jak přiřadit šablonu nákladu do nového nákladu.
author: Weijiesa
ms.date: 10/30/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLoadTemplate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: weijiesa
ms.search.validFrom: 2020-10-30
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 47b4925c528b64b835ce3e88659ee6ab0572eb2b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8844173"
---
# <a name="load-templates"></a>Šablony vytížení

[!include [banner](../../includes/banner.md)]

Při vytváření nového vytížení můžete přiřadit šablonu vytížení. Šablona vytížení obsahuje informace o vybavení a měrných jednotkách, jako je výška, šířka, hloubka a objem nákladu.

Tento článek popisuje způsob nastavení šablony nákladů a jak přiřadit šablonu nákladu do nového nákladu.

## <a name="set-up-a-load-template"></a>Nastavení šablony vytížení

1. Přejděte na **Řízení dopravy \> Nastavení \> Sestavení vytížení \> Šablona vytížení**.
1. V podokně akcí vyberte **Nová** pro přidání nové šablony nebo **Upravit** pro úpravu existující šablony.
1. V řádku pro novou nebo stávající šablonu nastavte následující pole:

    - **ID šablony vytížení** - Zadejte jedinečný identifikátor (ID) pro šablonu vytížení.
    - **Vybavení** - Vyberte vybavení, které by mělo být použito k přepravě nákladu.
    - **Výška nákladu**, **Šířka nákladu** a **Hloubka nákladu** - Zadejte rozměry nákladu.
    - **Maximální povolený objem nákladu** a **Maximální povolená hmotnost nákladu** - Zadejte maximální povolený objem a hmotnost nákladu.
    - **Maximální povolená hrubá hmotnost** - Zadejte maximální povolenou hrubou hmotnost nákladu. Hrubá hmotnost nákladu zahrnuje hmotnosti obalu a nákladovou hmotnost.
    - **Maximální počet kusů nákladu** - Zadejte maximální počet kusů, které může náklad obsahovat.
    - **Složení nákladu na zemi** - Zaškrtnutím tohoto políčka použijete nakládku na zemi. Ve scénáři nákladu na zemi jsou krabice seřazeny od podlahy ke stropu, od stěny ke stěně uvnitř kontejneru pro využití maximální kapacity.

1. V podokně akcí vyberte **Uložit**.

## <a name="associate-a-load-template-with-a-new-load"></a>Přiřazení šablony nákladu k novému nákladu

1. Přejděte do **Správa přepravy \> Plánování \> Pracovní plocha plánování vytížení**.
1. V horní části stránky vyberte jednu z následujících karet v závislosti na typu zdrojového dokumentu, pro který vytváříte náklad: **Dodávky**, **Řádky prodeje**, **Řádky převodu** nebo **Řádky nákupní objednávky**. 
1. Vyberte konkrétní dokument, pro který chcete naplánovat náklad.
1. V podokně Akce na kartě **Nabídka a poptávka** vyberte ve skupině **Přidat** možnost **Do nového vytížení**.
1. V dialogovém okně **Šablona vytížení** zvolte v poli **ID šablony vytížení** šablonu, kterou použijete.
1. Zvolte **OK** pro použití šablony.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]