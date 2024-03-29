---
title: Rozšíření aplikace Talent o Power Apps a Power Automate
description: Tento článek popisuje několik příkladů scénářů rozšíření pro aplikaci Microsoft Dynamics 365 Human Resources používající Microsoft Power Apps a Microsoft Power Automate.
author: negudava
ms.date: 02/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: negudava
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 5fe8ecd368bc63eed43c86053084ca67ef9beac6
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8859510"
---
# <a name="extend-with-power-apps-and-power-automate"></a>Rozšíření o Power Apps a Power Automate


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



Tento článek popisuje několik příkladů scénářů rozšíření pro aplikaci Microsoft Dynamics 365 Human Resources používající Microsoft Power Apps a Microsoft Power Automate. Můžete importovat balíček řešení přidružený ke každému příkladu do prostředí Power Apps. Poté můžete tyto balíčky použít pokyny jako návod nebo jako počáteční body pro implementaci scénářů, které jsou použitelné pro vaši organizaci.

> [!IMPORTANT]
> Pokud chcete používat šablony a aplikace, které jsou popsány v tomto článku „tak, jak jsou“, nezapomeňte je otestovat, abyste se ujistili, že pokrývají všechny scénáře, které jsou specifické pro vaši implementaci.

## <a name="prerequisites"></a>Předpoklady

- Pro import balíčků, musí mít uživatelé oprávnění **Tvůrce prostředí**.
- Pro export nebo import aplikací musí mít uživatelé licenci Power Apps Plan 2 nebo zkušební licenci Power Apps Plan 2.

## <a name="integration-with-microsoft-365-power-automate"></a>Integrace s aplikací Microsoft 365, Power Automate

Aplikaci **Integrace s Microsoft 365** lze použít k extrakci informací o týmu pro přihlášené uživatele z Microsoft 365. Uvádí zaměstnance v aplikaci Human Resources pro zjištění typů identifikace zaměstnanců. Manažeři mohou kontrolovat data vypršení platnosti typů ID zaměstnanců. Mohou také odeslat připomenutí e-mailem v případě, že končí platnost typu ID zaměstnance. Power Automate se integruje s Power Apps pro odeslání tohoto připomenutí. Po odeslání připomenutí bude odesláno potvrzení zpět do Power Apps z Power Automate. Typy identifikace zahrnují řidičský průkaz, cestovní pas a jiné přijatelné formy průkazů totožnosti.

Tuto aplikaci můžete rozšířit na další scénáře. Lze ji použít například pro zobrazení informací o dovolené týmu, událostech kalendáře a jakýchkoliv událostech specifických pro tým.

Chcete-li stáhnout **Integraci s aplikací Microsoft 365, Power Automate**, přejděte na stránku [Integrace s Microsoft 365](https://go.microsoft.com/fwlink/?linkid=2081787) na stránce Microsoft Download Center.

## <a name="power-automate--sql-connect-and-execute"></a>Power Automate – připojení k SQL a provedení

Šablona **Power Automate – připojení k SQL a provedení** se připojuje k serveru Microsoft SQL Server a povoluje spuštění SQL dotazů.

Přestože tato šablona čte a aktualizuje tabulky SQL, můžete ji rozšířit a použít pro jiné scénáře. Například ji můžete použít k vyplnění tabulky fázování v Dataverse záznamy z SQL Serveru a pravidelné synchronizaci tabulky fázování pomocí přírůstkového nabízení z SQL Serveru.

Rozšířený dotaz je integrován s tokem za účelem povolení transformace dat a přírůstkového nabízení.

Chcete-li stáhnout šablonu **Power Automate – připojení k SQL a provedení**, přejděte na [Power Automate – připojení k SQL a provedení](https://go.microsoft.com/fwlink/?linkid=2081789) v Microsoft Download Center.

## <a name="additional-resources"></a>Další prostředky

[Microsoft Power Platform](/power-platform/admin/admin-documentation)</br>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
