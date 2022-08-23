---
title: Konfigurace prostředí služeb a připojených aplikací
description: Tento článek poskytuje informace o tom, jak nakonfigurovat prostředí služeb a připojené aplikace.
author: gionoder
ms.date: 02/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.custom: 97423,  ""intro-internal
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: 8ede98cfad685992bad3fb643ea46d6adcb08487
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9269524"
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
