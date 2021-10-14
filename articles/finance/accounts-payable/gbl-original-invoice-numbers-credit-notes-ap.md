---
title: Odkazy na původní faktury v dobropisech (faktur dodavatele)
description: Toto téma popisuje, jak při vytváření dobropisu vytvořit odkaz na původní fakturu.
author: v-oloski
ms.date: 09/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: v-oloski
ms.search.validFrom: 2021-09-23
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 6114ffb4d3b9e942887cbfa10c6039b0d73af7e1
ms.sourcegitcommit: 86f0574363fb869482ef73ff294f345f81d17c5b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/29/2021
ms.locfileid: "7562219"
---
# <a name="reference-original-invoices-in-credit-notes-vendor-invoices"></a>Odkazy na původní faktury v dobropisech (faktur dodavatele)

[!include [banner](../includes/banner.md)]

Toto téma popisuje, jak při vytváření dobropisu vytvořit odkaz na původní fakturu.

## <a name="prerequisites"></a>Předpoklady

V pracovním prostoru **Správa funkcí** zapněte funkci **Povolit opravnou fakturaci u faktur dodavatele**. Další informace naleznete v tématu [Přehled správy funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

Funkce popsané v tomto tématu platí pro následující obchodní dokumenty:

**Závazky:**

- Nákupní objednávka
- Deník faktur
- Registr faktur

**Hlavní kniha:**

- Hlavní deník

## <a name="define-a-reference-to-an-original-invoice"></a>Definování odkazu na původní fakturu

Pomocí následujících postupů definujte odkaz na původní fakturu na základě konkrétního typu obchodního dokumentu.

### <a name="vendor-credit-note-purchase-order"></a>Dobropis dodavatele (nákupní objednávka)

1. Přejděte na **Závazky** \> **Nákupní objednávky** \> **Všechny nákupní objednávky**.
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
