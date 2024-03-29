---
title: Nastavení elektronické fakturace
description: Tento článek poskytuje přehled procesu nastavení a konfigurace elektronické fakturace.
author: gionoder
ms.date: 02/28/2022
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
ms.openlocfilehash: de94843c1e98a8788375bd41def587a64baea07d
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9272172"
---
# <a name="electronic-invoicing-setup"></a>Nastavení elektronické fakturace

[!include [banner](../includes/banner.md)]

Tento článek poskytuje přehled procesu nastavení a konfigurace elektronické fakturace. Kroky nastavení musíte provést v pořadí, které je zde specifikováno. Pokud je krok povinný, ale vy jej přeskočíte, funkce nebude fungovat správně a během následujících kroků nebo při použití funkce dojde k více selháním. 

Než začnete, ujistěte se, že jsou všechny hlavní součásti správně nastaveny, že jste se zaregistrovali ke službě Regulatory Configuration Service (RCS) a máte instanci RCS a že je nainstalován doplněk pro elektronickou fakturaci pro vaše prostředí Microsoft Dynamics 365 Finance nebo Dynamics 365 Supply Chain Management. Více informací viz [Registrace a instalace elektronické fakturace](e-invoicing-install-add-in-microservices-lcs.md).

Dále nastavte prostředky Azure, které elektronická fakturace vyžaduje ke své práci. Další informace viz [Nastavení zdrojů Azure pro elektronickou fakturaci](e-invoicing-set-up-azure-resources.md).

Po nakonfigurování hlavních komponent pracujte s RCS a nastavte hlavní logické komponenty elektronické fakturace. Nejprve definujte počet servisních prostředí, která budete udržovat. Tímto způsobem definujete dělení logických dat a konfigurace, abyste zajistili, že máte hranici mezi vývojovým nebo testovacím prostředím a produkčním prostředím. Chcete-li nastavit proces vývoje flexibilně, možná budete potřebovat několik samostatných vývojových a testovacích prostředí. Kromě definování prostředí služeb nastavte přímo z RCS odkaz na své podnikové aplikace, jako je Finance nebo Supply Chain Management, a nastavte parametry, které jsou nutné pro správnou funkci elektronické fakturace. Další informace o prostředích naleznete v části [Prostředí služeb](e-invoicing-service-environments.md).

Poté, co je vše nastaveno, můžete vytvořit vlastní funkce globalizace, které definují různé scénáře pro zpracování elektronických dokumentů a transformaci dat nebo pro import dokumentů z globálního úložiště. Další informace, jak pracovat s funkcemi globalizace, viz [Práce s funkcemi globalizace](e-invoicing-working-globalization-features.md).

Pokud vaše scénáře vyžadují integraci s e-mailem nebo SharePoint pro zpracování příchozích elektronických dokumentů, viz [Zpracování příchozích elektronických dokumentů](e-invoicing-process-incoming-electronic-documents.md), kde najdete informace o tom, jak tyto kanály nastavit a používat.
