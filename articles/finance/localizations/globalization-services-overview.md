---
title: Globalizační služby Dynamics 365
description: Toto téma poskytuje přehled globalizačních služeb Microsoft Dynamics 365.
author: JaneA07
ms.date: 04/12/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: RCS, Regulatory Configuration Services, Localization, Electronic invoicing, Tax calculation
audience: Application User
ms.reviewer: kfend
ms.custom:
- "97423"
- intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 1dfe88bf6eb0cf479f8febd8a599b165b71d932d
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2022
ms.locfileid: "7985984"
---
# <a name="dynamics-365-globalization-services"></a>Globalizační služby Dynamics 365

[!include [banner](../includes/banner.md)]

Následující globalizační služby lze nakonfigurovat tak, aby rozšířily možnosti, které existují v některých online službách Microsoft Dynamics 365:

- **Regulatory Configuration Service (RCS)** podporuje konfiguraci různých typů elektronických dokumentů a zpráv. RCS poskytuje vylepšenou verzi návrháře elektronického výkaznictví (ER), kde je úložiště konfigurace samostatnou službou. Další informace viz [Regulatory Configuration Service](rcs-overview.md).
- **Elektronická fakturace** sdružuje konfigurovatelné formáty pro transformace, digitální podpisy a konfigurovatelné integrace pro připojení k externím webovým službám, včetně certifikace a zpracování odpovědí. Další informace získáte v tématu [Elektronická fakturace](e-invoicing-service-overview.md).
- **Výpočet daně** poskytuje zvýšenou flexibilitu podporou více daňových identifikačních čísel, určování daňových zákonů, návrháře výpočtu daní a modulu runtime, který vyhovuje celosvětovým komplexním daňovým předpisům. Další informace naleznete v tématu [Výpočet daně](global-tax-calcuation-service-overview.md).

Tyto globalizační služby poskytují okamžitou integraci s následujícími online službami Dynamics 365.

| Online služba | RCS | Elektronická fakturace | Výpočet daně (Preview) |
|----------------|-----|----------------------|---------------------------|
| Dynamics 365 Finance | Ano | Ano | Ano | 
| Dynamics 365 Supply Chain Management | Ano | Ano | Ano | 
| Dynamics 365 Project Operations | Ano | Ano | Nelze použít | 
| Dynamics 365 Commerce | Ano | Nelze použít | Nelze použít | 

> [!NOTE]
> Z důvodu rozdílů v dostupnosti geografických lokalit Azure (geos) pro RCS může konfigurace této služby způsobit, že se údaje o zákaznících přenesou mimo geografickou oblast vybranou pro příslušnou online službu Dynamics 365. Další informace najdete v části [Dynamics 365 a Power Platform: Dostupnost, umístění dat, jazyk a lokalizace](https://aka.ms/rcs/D365Productavailabilityguide).