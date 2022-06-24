---
title: Konfigurace prostředí služeb a připojených aplikací
description: Tento článek poskytuje informace o tom, jak nakonfigurovat prostředí služeb a připojené aplikace.
author: dkalyuzh
ms.date: 02/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom:
- "97423"
- intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: c1bb3f784148f04c01223ac4e280a18bacfe0e51
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8853215"
---
# <a name="configure-service-environments-and-connected-applications"></a>Konfigurace prostředí služeb a připojených aplikací

[!include [banner](../includes/banner.md)]

Tento článek poskytuje informace o tom, jak nakonfigurovat prostředí služeb a připojené aplikace. Tento proces má tři kroky. Krok 1 je povinný, kroky 2 a 3 jsou volitelné.

## <a name="step-1-create-a-service-environment"></a>Krok 1: Vytvoření servisního prostředí

Když vytváříte prostředí služeb, definujte seznam uživatelů, kteří do něj mohou nasadit funkce globalizace. Volitelně u některých scénářů definujte seznam externích aplikací, které mohou komunikovat se službou Elektronická fakturace. Nastavte číselné řady, pokud je budete používat ve svých scénářích.

Dokončení tohoto kroku proveďte dle tématu [Prostředí služeb](e-invoicing-service-environments.md).

## <a name="step-2-add-certificates-and-secrets"></a>Krok 2: Přidání certifikátů a tajných kódů

Přidejte odkaz na trezor klíčů Microsoft Azure a tajné kódy, abyste je mohli použít ve svých scénářích. Tento krok je povinný, pokud akce v kanálech zpracování používají certifikáty a tajné kódy pro digitální podepisování nebo komunikaci s externími webovými službami.

Dokončení tohoto kroku proveďte dle tématu [Zákaznické certifikáty a tajné kódy](e-invoicing-customer-certificates-secrets.md).

## <a name="step-3-configure-connected-applications"></a>Krok 3: Konfigurace připojených aplikací

Chcete-li nastavit komunikaci mezi aplikacemi Dynamics 365 Finance nebo Dynamics 365 Supply Chain Management a Elektronickou fakturací, musíte nakonfigurovat Finance nebo Supply Chain Management tak, aby vytvořily volání služby Elektronická fakturace a připravily obchodní data v jednotné struktuře, kterou lze transformovat do požadovaného elektronického formátu. Aplikace také musí správně zpracovávat odpovědi ze služby. Tuto konfiguraci můžete dokončit přímo v prostředí Finance nebo Supply Chain Management, nebo ji můžete dokončit ve službě Regulatory Configuration Service (RCS). Pokud dokončíte konfiguraci v RCS, můžete ji nasadit do prostředí Finance nebo Supply Chain Management. V tomto kroku zaregistrujete připojenou aplikaci pro nasazení parametru.

Dokončení tohoto kroku proveďte dle tématu [Připojené aplikace](e-invoicing-connected-applications.md).
