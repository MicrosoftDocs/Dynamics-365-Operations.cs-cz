---
title: Skenování čárových kódů pomocí fotoaparátu v aplikaci Dynamics 365 for Finance and Operations – sklady
description: Toto téma vysvětluje, jak nastavit Dynamics 365 for Finance and Operations – Sklady pro skenování čárových kódů pomocí fotoaparátu na mobilním zařízení.
author: MarkusFogelberg
manager: AnnBe
ms.date: 01/03/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSMobileAppField
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2017-01-03
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: e78d0a82d3ca66a6912ea1a9517296ca241edf1c
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "319424"
---
# <a name="scan-bar-codes-using-a-camera-in-dynamics-365-for-finance-and-operations--warehousing"></a>Skenování čárových kódů pomocí fotoaparátu v aplikaci Dynamics 365 for Finance and Operations – sklady

[!include [banner](../includes/banner.md)]

Toto téma vysvětluje, jak nastavit Dynamics 365 for Finance and Operations – Sklady pro skenování čárových kódů pomocí fotoaparátu na mobilním zařízení. 

## <a name="prerequisites"></a>Požadavky
Chcete-li použít tuto funkci, musíte mít nainstalovanou verzi 1.2.0.0 aplikace Sklady a vaše zařízení musí mít fotoaparát. Když otevřete aplikaci po aktualizaci, budete vyzváni, abyste povolili aplikaci Dynamics 365 for Finance and Operations – Sklady použít fotoaparát. Pokud vaše zařízení nemá fotoaparát, nezobrazí se výzva a nebude možné používat fotoaparát jako skener. 

## <a name="setup"></a>Nastavení
V nastavení displeje aplikace Sklady můžete vybrat, zda má být použit fotoaparát ke skenování čárových kódů. Pokud povolíte možnost **Použít fotoaparát jako skener**, lze použít fotoaparát pro každé pole pro zadávání s upřednostňovaným vstupním režimem nastaveným na **Skenování**. 

K určení, zda vstupní pole má být skenovatelné, nastavte na stránce **Názvy polí aplikace Sklady** v Dynamics 365 for Finance and Operations **Upřednostňovaný režim vstupu** na **Skenování**. Pokud je vybrána tato možnost, fotoaparát slouží pro skenování v aplikaci Sklady. Informace o způsobu konfigurace názvů polí aplikace Sklady naleznete v tématu [Konfigurace názvů polí v aplikaci Sklady](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/warehousing/configure-app-field-names-priorities-warehouse).

## <a name="supported-bar-code-formats"></a>Podporované formáty čárového kódu
Jsou podporovány nejběžnější formáty čárového kódu, včetně kódu 128, kódu 39, kódu 93, EAN-8, EAN-13, UPC-E, UPC-A a QR kódů 

## <a name="navigation"></a>Navigace
Stránka fotoaparátu bude spuštěna na každé stránce, kde má vstupní pole preferovaný vstupní režim nastavený na Skenování. Když se nacházíte na stránce fotoaparátu, použijte pro navigaci následující možnosti:
- Klikněte na tlačítko Zpět pro návrat na stránku úloh a podrobností. 
- Klikněte na ikonu tužky na stránce úloh a podrobností a přejděte na stránku, kde můžete zadávat vstup ručně.
- Klikněte na ikonu fotoaparátu na stránce úloh a podrobností pro návrat na stránku fotoaparátu. 

| Stránka úloh a podrobností | Stránka fotoaparátu | 
| :---------------------: | :--------------------: |
| ![camera-scanning-example-task-detail-page](./media/camera-scanning-example-task-detail-page50.png)          | ![camera-scanning-example-camera-page-smaller](./media/camera-scanning-example-camera-page50.png)          |

Na stránce fotoaparátu po kliknutí na tlačítko fotoaparátu bude toto tlačítko šedé při pokusu o identifikaci čárového kódu. Pokud čárový kód není identifikován do 5 sekund, proces vyprší a tlačítko fotoaparátu bude opět dostupné. Budete pak moci se pokusit znovu o naskenování čárového kódu.

Jestliže zaměříte fotoaparátu na čárový kód, udržujte čárový kód zarovnaný mezi čarami pro dosažení nejlepších výsledků. Při úspěšném naskenování čárového kódu bude zpracován výsledek a budete navedeni k dalšímu kroku. Pokud další krok obsahuje jiné vstupní pole s upřednostňovaným vstupním režimem nastaveným na Skenování, stránka fotoaparátu se znovu spustí. Pokud není dalším krokem skenovací pole, stránka kamery se nespustí.

