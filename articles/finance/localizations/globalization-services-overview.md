---
title: Globalizační služby Dynamics 365
description: Toto téma poskytuje přehled globalizačních služeb Microsoft Dynamics 365.
author: JaneA07
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RCS, Regulatory Configuration Services, Localization, Electronic invoicing, Tax calculation
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 2ef942f7f6dac2c321a51800ade0bf25f2162304
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018800"
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