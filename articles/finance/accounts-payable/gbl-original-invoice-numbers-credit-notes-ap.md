---
title: Odkazy na původní faktury v dobropisech (faktur dodavatele)
description: Tento článek popisuje, jak při vytváření dobropisu vytvořit odkaz na původní fakturu.
author: AdamTrukawka
ms.date: 09/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: atrukawk
ms.search.validFrom: 2021-09-23
ms.dyn365.ops.version: 10.0.20
ms.search.form: ''
ms.openlocfilehash: 39cf4eb7eef1a83abeb7bd44fa7b2abefee0806e
ms.sourcegitcommit: 8eb0cafe5ad20be2c4fff684e88d7d3f2249f820
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/06/2022
ms.locfileid: "9409657"
---
# <a name="reference-original-invoices-in-credit-notes-vendor-invoices"></a>Odkazy na původní faktury v dobropisech (faktur dodavatele)

[!include [banner](../includes/banner.md)]

V některých zemích a regionech existuje zákonný požadavek, aby tištěné dobropisy nebo postupy hlášení obsahovaly odkazy na původní faktury. Tento článek popisuje, jak při vytváření dobropisu vytvořit odkaz na původní fakturu.

## <a name="prerequisites"></a>Předpoklady

V pracovním prostoru **Správa funkcí** zapněte funkci **Povolit opravnou fakturaci u faktur dodavatele**. Další informace naleznete v tématu [Přehled správy funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

Funkce popsané v tomto článku platí pro následující obchodní dokumenty:

**Závazky:**

- Nákupní objednávka
- Deník faktur
- Registr faktur

**Hlavní kniha:**

- Hlavní deník

## <a name="define-a-reference-to-an-original-invoice"></a>Definování odkazu na původní fakturu

Definování odkazu na původní fakturu zahrnuje následující základní kroky:
1. Vytvořte a zaúčtujte fakturu dodavatele.
2. Vytvořit dobropis dodavatele.
3. Pomocí funkce Opravná fakturace propojit fakturu s dobropisem.
4. Zaúčtovat dobropis.

Pomocí následujících postupů definujte odkaz na původní fakturu na základě konkrétního typu obchodního dokumentu.

### <a name="vendor-credit-note-purchase-order"></a>Dobropis dodavatele (nákupní objednávka)

1. Přejděte na **Závazky** > **Nákupní objednávky** > **Všechny nákupní objednávky**.
2. Vytvořte novou nákupní objednávku nebo použijte stávající k vytvoření dobropisu.
3. V podokně akcí na kartě **Faktura** ve skupině **Zadat** zvolte **Opravná fakturace**.
4. Zadejte důvod opravy a odkaz na původní fakturu.

### <a name="vendor-credit-note-ledger-journals"></a>Dobropis dodavatele (deníky hlavní knihy)

1. Proveďte jeden z následujících kroků:

    - Přejděte na **Závazky** \> **Deníky faktur**.
    - Přejděte na **Závazky** \> **Registr faktur**.
    - Přejděte do nabídky **Hlavní kniha** \> **Položky deníku** \> **Hlavní deníky**.

2. Vytvořte nový deník a řádky nového deníku.
3. V podokně akcí vyberte **Funkce** \> **Opravná fakturace**.
4. Zadejte důvod opravy a odkaz na původní fakturu.

> [!NOTE]
> Příkaz **Opravná fakturace** je viditelný v dokladu hlavního deníku, pokud je **Typ účtu** nastaven na **Dodavatel**.
