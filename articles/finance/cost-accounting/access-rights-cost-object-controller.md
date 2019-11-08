---
title: Definování přístupových práv pro kontrolory objektů nákladů
description: Toto téma poskytuje informace o přístupových právech pro kontrolory objektů nákladů.
author: AndersGirke
manager: AnnBe
ms.date: 06/24/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMCostControlWorkspace, CAMParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: e86f087a1df0f133dbaa5491cf5ba9e57b0e12d9
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/03/2019
ms.locfileid: "2551719"
---
# <a name="define-access-rights-for-cost-object-controllers"></a>Definování přístupových práv pro kontrolory objektů nákladů

[!include [banner](../includes/banner.md)]

Pracovní prostor **Řízení nákladů** je centrální bod, kde si mohou manažeři zobrazit výkonnost svých objektů nákladů. Tento pracovní prostor umožňuje manažerům využít data nákladového účetnictví, i když nejsou nákladovými účetními. Z důvodu bezpečnosti by mělo být dovoleno manažerům zobrazovat pouze data nákladového účetnictví, která se vztahují ke konkrétním objektům nákladů, za které jsou zodpovědní.

Existují čtyři jedinečné role v nákladovém účetnictví.

| Název role               | Licence      |
|-------------------------|--------------|
| Správce nákladového účetnictví | Aktivita     |
| Nákladový účetní         | Operations   |
| Úředník na pozici nákladového účetního   | Operations   |
| Kontrolor objektu nákladů  | Členové týmu |

Toto téma vysvětluje, jak přiřadit manažerovi roli **Kontrolor objektu nákladů**.

Když je manažerovi přiřazena role **Kontrolor objektu nákladů**, může manažer provádět následující úkoly:

- Přistupovat k pracovnímu prostoru **Řízení nákladů** (v klientovi).

    - Procházet a mít přístup pro zobrazení ke stránkám, které podporují podrobné procházení.

- Přistupovat k pracovnímu prostoru **Řízení nákladů** (v mobilní aplikaci).

> [!NOTE]
> **Náklady objektu řízeného** role není řízení nákladů, které předměty má uživatel přístup a zobrazit data pro. Zabezpečení na úrovni řádku je poskytováno prostřednictvím hierarchií dimenzí a hierarchie přístupového seznamu.

## <a name="grant-access-rights"></a>Udělení přístupových práv
Následující příklad ukazuje, jak může vypadat hierarchie dimenzí.

**Podrobnosti hierarchie dimenze**

| Název hierarchie dimenze | Dimenze    | Název typu hierarchie dimenze      | Hierarchie přístupového seznamu |
|--------------------------|--------------|------------------------------------|-----------------------|
| Organizace             | Nákladová střediska | Hierarchie klasifikace dimenzí | **Ano**               |

Můžete použít pevnou záložku **Uživatelé** v návrháři hierarchie, abyste vložili jedno nebo více ID uživatele na každém uzlu.

|                                   | Uživatelé            | Rozsahy členu dimenze   |                         |
|-----------------------------------|------------------|---------------------------|-------------------------|
| **Uzly**                         | **ID uživatele**      | **Od členu dimenze** | **Po člen dimenze** |
| Organizace                      | Benjamin, Claire |                           |                         |
| &nbsp;&nbsp;Správce                 | Duben            |                           |                         |
| &nbsp;&nbsp;&nbsp;&nbsp;Finance   | Alicia           | CC002                     | CC003                   |
|                                   |                  | CC007                     | CC007                   |
| &nbsp;&nbsp;&nbsp;&nbsp;HR        | Arnie            | CC001                     | CC001                   |
| &nbsp;&nbsp;Výroba            | David            |                           |                         |
| &nbsp;&nbsp;&nbsp;&nbsp;Balení | Ellen            | CC005                     | CC005                   |
| &nbsp;&nbsp;&nbsp;&nbsp;Sestavení  | Chris            | CC006                     | CC006                   |

> [!NOTE]
> Nákladoví účetní musí být přiřazeni do hierarchie nejvyšší úrovně, aby mohli nahlížet do všech položek nákladového účetnictví.

Než bude možné použít hierarchii přístupového seznamu a jeho bezpečnostní nastavení, musí být možnost **Povolit přístup k zobrazení pro členy dimenze objektu nákladů** nastavena na **Ano** na kartě **Obecné** na stránce **Parametry nákladového účetnictví** (**Nákladové účetnictví** > **Nastavení** > **Parametry**).

Nastavení pro hierarchii přístupového seznamu se používají ke kontrole dat, zobrazených v následujících oblastech:

- Pracovní prostor **Řízení nákladů** (v klientovi):

    - Data na stránkách, které se používají k podrobnému prohlížení

- Pracovní prostoru **Řízení nákladů** (v mobilní aplikaci):

    - Zůstatky na kartách

- Microsoft Power BI:

    - Data zobrazená ve vizualizacích Power BI
    - Vizualizace dat Power BI, které jsou vloženy do klienta Dynamics 365 Finance

> [!IMPORTANT]
> - Než může hierarchie přístupového seznamu ovlivnit data v Power BI, musí být spárována hierarchie přístupového seznamu a zabezpečení na úrovni řádku v Power BI. Další informace naleznete v tématu [Nastavení zabezpečení pro balíček obsahu nákladového účetnictví](../../dev-itpro/analytics/setup-security-cost-accounting-content-pack.md).
> - Toto téma popisuje požadavky, které musí být splněny před použitím pracovního prostoru **Řízení nákladů**.

Další zdroje

- [Pracovní prostor kontroly nákladů](cost-control-workspace.md)
- [Hierarchie dimenzí](dimension-hierarchy.md)
- [Nastavení zabezpečení pro balíček obsahu nákladového účetnictví](../../dev-itpro/analytics/setup-security-cost-accounting-content-pack.md)