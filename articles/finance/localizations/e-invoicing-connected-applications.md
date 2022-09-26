---
title: Připojené aplikace
description: Tento článek vysvětluje nastavení připojených aplikací v Elektronické fakturaci.
author: gionoder
ms.date: 02/07/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: aa6c80914301cc0403974a6acc5e95ff61c9c1a7
ms.sourcegitcommit: a5a4c45bb265758c6e5c3483c8552503b1799a89
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/16/2022
ms.locfileid: "9524682"
---
# <a name="connected-applications"></a>Připojené aplikace

[!include [banner](../includes/banner.md)]

Připojené aplikace jsou instance aplikací Microsoft Dynamics 365 Finance a Dynamics 365 Supply Chain Management, ke kterým se můžete připojit prostřednictvím služby Regulatory Configuration Service (RCS). Prostřednictvím připojených aplikací můžete nakonfigurovat část vaší funkce globalizace v aplikacích Finance nebo Supply Chain Management, aby byl funkční celý scénář Elektronické fakturace.

Když nasadíte svou funkci Globalizace, informace o nastavení, které jsou použitelné pro vaši aplikaci Finance nebo Supply Chain Management, lze publikovat přímo z RCS do příslušné připojené aplikace.

Dostupnost parametrů aplikací Finance nebo Supply Chain Management v RCS je užitečná, když máte několik aplikačních prostředí, jako je uživatelské akceptační testování (UAT) a produkční prostředí, a chcete zachovat konzistentní nastavení nasazením stejných parametrů do různých prostředí.

## <a name="create-a-connected-application"></a>Vytvoření propojené aplikace

1. Přihlaste se k účtu RCS.
2. V pracovním prostoru **Funkce globalizace** v části **Související odkazy** vyberte dlaždici **Nastavení prostředí**.
3. Na stránce **Nastavení prostředí** v podokně akcí vyberte **Propojené aplikace**.
4. Zvolte **Nový** pro vytvoření propojené aplikace.
5. Do pole **Název** zadejte název aplikace, ke které se má provést připojení.
6. V poli **Typ** zvolte **Dynamics 365 Finance**.
7. Do pole **Aplikace** zadejte adresu URL prostředí, ke kterému se má provést připojení.
8. V poli **Klient** zadejte klienta prostředí.
9. Zvolte možnost **Uložit**.
10. V podokně akcí vyberte **Zkontrolovat připojení**, abyste otestovali spojení s prostředím. Poté stránku zavřete.

## <a name="link-connected-applications-to-environments"></a>Propojení připojených aplikace s prostředím

1. Na stránce **Nastavení prostředí** vyberte **Nový** a přiřaďte připojenou aplikaci prostředí.
2. V poli **Připojená aplikace** vyberte připojenou aplikaci.
3. V poli **Prostředí služby** vyberte prostředí služeb.
4. Zvolte **Uložit** a pak zavřete stránku.
