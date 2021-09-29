---
title: Archivovat vytištěné faktury zákazníků s hash čísly
description: Toto téma vysvětluje, jak povolit archivaci, aby bylo možné ukládat tištěné faktury zákazníků s čísly hash.
author: ilkond
ms.date: 09/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 539093
ms.search.region: Global
ms.author: ilyako
ms.search.validFrom: 2021-03-05
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 093b1b8c516c0c659e7970d17d3f84b2ed0ccf8f
ms.sourcegitcommit: ecd4c148287892dcd45656f273401315adb2805e
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/18/2021
ms.locfileid: "7500520"
---
# <a name="archive-printed-customer-invoices-with-hash-numbers"></a>Archivovat vytištěné faktury zákazníků s hash čísly

[!include [banner](../includes/banner.md)]

V některých zemích existuje zákonný požadavek ukládat vypočítaná čísla hash v systému společně s výtisky některých dokumentů. Čísla hash lze použít pro hlášení orgánům a během auditů.

Toto téma vysvětluje, jak konfigurovat archivaci, aby bylo možné ukládat tištěné faktury zákazníků s čísly hash.

## <a name="prerequisites"></a>Předpoklady

- V pracovním prostoru **Správa funkcí** zapněte funkci **Archivovat vytištěné faktury zákazníků s hashovými čísly**. Další informace naleznete v tématu [Přehled správy funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).
- Nakonfigurujte tiskové formáty požadovaných dokumentů v části **Správa tisku**.

Tato funkce se vztahuje na následující dokumenty.

**Pohledávky**
- Faktura zákazníka
- Dobropis zákazníkům
- Volné faktury
- Dobropis s volným textem

**Řízení projektů a účetnictví**
- Faktura projektu
- Dobropis projektu

## <a name="configure-customer-master-data"></a>Konfigurace hlavních dat zákazníků
Chcete-li nakonfigurovat údaje o zákazníkovi a zapnout možnost automatického ukládání tištěných faktur jako přílohy, proveďte následující kroky.

1. Přejděte na **Pohledávky** > **Všichni zákazníci**. 
2. Vyberte zákazníka a na kartě s náhledem **Faktura a doručení** v části **ELEKTRONICKÁ FAKTURA** v poli **Příloha e-faktury** vyberte **Ano**.

## <a name="print-invoices"></a>Tisk faktur
Můžete zaúčtovat a vytisknout libovolný volný text, zákaznickou a projektovou fakturu nebo dobropis pro zákazníka nakonfigurovaný v předchozím postupu.

Otevřete stránku **Přílohy** pro vytištěnou fakturu. Na kartě s náhledem **Příloha** ve skupině polí **Další detaily** poli v **Číslo hash dokumentu** vyhledejte uložené hash číslo vypočítané pro vytištěnou fakturu.

![Hash číslo přílohy.](media/attach-hash-num.jpg)

