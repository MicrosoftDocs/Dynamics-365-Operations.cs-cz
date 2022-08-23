---
title: Přihlášení a instalace služby Elektronické fakturace
description: Tento článek poskytuje informace o tom, jak se přihlásit ke službě elektronické fakturace a nainstalovat ji.
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
ms.openlocfilehash: 99f484e5ab8821c78fde776a9d3195dade2a09d5
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9283950"
---
# <a name="sign-up-for-and-install-the-electronic-invoicing-service"></a>Přihlášení a instalace služby Elektronické fakturace

[!include [banner](../includes/banner.md)]

Tento článek poskytuje informace o tom, jak se přihlásit ke službě elektronické fakturace a nainstalovat ji. Tento proces má čtyři kroky. Kroky 1 až 3 jsou povinné a krok 4 je volitelný.

### <a name="step-1-sign-up-for-regulatory-configuration-service"></a>Krok 1: Přihlaste se ke službě Regulatory Configuration Service

Regulatory Configuration Service (RCS) poskytuje konfiguraci a prostředí návrhu, které se používá ke konfiguraci elektronické fakturace. Prostředky typu prostředí nebo funkce elektronické fakturace jsou vytvářeny, udržovány a spravovány v RCS. Když jsou prostředky připraveny, jsou publikovány ve službě elektronické fakturace.

Pro více informací o RCS viz [Regulatory Configuration Services (RCS) – funkce globalizace](rcs-globalization-feature.md).

Můžete se zaregistrovat do RCS ze [stránky Regulatory Configuration Service](https://marketing.configure.global.dynamics.com/).

### <a name="step-2-install-the-add-in-for-microservices-in-microsoft-dynamics-lifecycle-services"></a>Krok 2: Instalace doplňku pro mikroslužby ve službě Microsoft Dynamics Lifecycle Services

Služba Elektronická fakturace je sada mikroslužeb, která je hostována v datových centrech společnosti Microsoft. Ve výchozím nastavení zákazníci Dynamics 365 Finance a Dynamics 365 Supply Chain Management nemají přístup ke službě Elektronická fakturace. Musíte ji nainstalovat jako doplněk v Microsoft Dynamics Lifecycle Services (LCS). Při instalaci doplňku se vaše prostředí Finance nebo Supply Chain Management zaregistruje v registru aplikací, které se mohou připojit ke službě Elektronická fakturace.

K provedení tohoto kroku viz [Instalace doplňku pro mikroslužby ve službě Lifecycle Services](e-invoicing-install-add-in-microservices-lcs.md).

### <a name="step-3-set-up-rcs"></a>Krok 3: Nastavte RCS

Musíte nastavit integraci mezi RCS a službou elektronické fakturace. Musíte také nastavit hlavní komponenty.

Pro dokončení tohoto kroku viz [Nastavení Regulatory Configuration Service (RCS)](e-invoicing-set-up-rcs.md).

### <a name="step-4-microsoft-power-platform-plug-in-admin-reference"></a>Krok 4: Reference správce modulu plug-in Microsoft Power Platform

Některé scénáře vyžadují integraci s Dataverse v rozsahu Microsoft Power Platform.

V současné době je toto nastavení povinné, pokud budete používat řešení elektronické fakturace pro scénáře elektronické fakturace v Indonésii. Pro scénáře elektronické fakturace v Saúdské Arábii je však volitelný. Další informace najdete v tématu [Dostupnost funkcí elektronické fakturace podle země nebo regionu](e-invoicing-country-specific-availability.md).

Pro dokončení tohoto kroku viz [Reference správce plug-inu Microsoft Power Platform](e-invoicing-power-platform-plug-in.md).
