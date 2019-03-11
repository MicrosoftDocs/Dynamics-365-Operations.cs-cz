---
title: Parametry integrace Project Service Automation
description: Toto téma vysvětluje, jak nakonfigurovat výchozí data zadávaná při integraci Microsoft Dynamics 365 for Project Service Automations Microsoft Dynamics 365 for Finance and Operations.
author: KimANelson
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 33960a97f69d6bcc70a3035d4d68095ca6993a10
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "347047"
---
# <a name="project-service-automation-integration-parameters"></a>Parametry integrace Project Service Automation

[!include[banner](../includes/banner.md)]

Na stránce **Parametry integrace Project Service Automation** můžete nakonfigurovat způsob zadávání výchozích dat při integraci aplikací Microsoft Dynamics 365 for Project Service Automation a Microsoft Dynamics 365 for Finance and Operations. Následující pole musí být nastaveny pro projekty, aby byly synchronizovány úspěšně z aplikace Project Service Automation do aplikace Finance and Operations.

> [!NOTE]
> - Integrace úkolů projektu, kategorie transakce výdajů, odhady hodin, odhady výdajů a uzamykání funkcí jsou k dispozici v aplikaci Microsoft Dynamics 365 for Finance and Operations verze 8.0.
> - Integrace skutečných hodnot je k dispozici v Microsoft Dynamics 365 for Finance and Operations verze 8.0.1 nebo pozdější.
> - Pokud používáte Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0, po instalaci KB 4132657 a KB 4132660 bude možné použít šablony k integraci projektových úkolů, kategorií transakcí výdajů, odhadů hodin, odhadů výdajů a skutečných hodnot a ke konfiguraci funkce uzamčení. Pokud musíte resetovat rozúčtování, doporučili jsme nainstalovat též KB 4131710.

| Karta                    | Pole                | popis |
|------------------------|----------------------|-------------|
| Obecný                | Výchozí typ projektu | Vyberte výchozí typ projektu. Pokud se projekty synchronizují z aplikace Project Service Automation, použije se tato hodnota, když jste nezadali výchozí hodnotu v šabloně integrace. Během synchronizace je pole **Typ projektu** nových projektů nastaveno na tuto hodnotu. Hodnota však může být aktualizována, když jsou řádky projektové smlouvy synchronizovány z Project Service Automation. |
|                        | Kategorie času        | Vyberte výchozí kategorii času. Tato hodnota se používá, když jsou odhady hodin synchronizovány z Project Service Automation. Když se synchronizují odhady hodin a skutečné hodnoty hodin z Project Service Automation, pole **Kategorie** prognózy hodin nových projektů v aplikaci Finance and Operations bude nastaveno na tuto hodnotu. |
|                        | Kategorie poplatku         | Vyberte výchozí kategorii poplatku. Tato hodnota se používá, když jsou skutečné hodnoty poplatků synchronizovány z Project Service Automation. Když se synchronizují skutečné hodnoty poplatků z Project Service Automation, pole **Kategorie** nových transakcí poplatků v aplikaci Finance and Operations bude nastaveno na tuto hodnotu. |
| Výchozí hodnoty skupiny projektu | Typ projektu         | Klikněte na **Nový** a přidejte řádek, kde můžete vybrat typ projektu, pro který chcete nastavit výchozí skupiny projektů. Konkrétní typ projektu lze vybrat pouze jednou v konfiguraci. |
|                        | Skupina projektu        | Vyberte výchozí skupinu projektů pro zvolený typ projektu. Když se z aplikace Project Service Automation. synchronizují nové projekty, pole **Skupina projektu** bude nastaveno na výchozí hodnotu pro typ projektu, pokud jste nezadali výchozí hodnotu v šabloně integrace. |
| Výchozí hodnoty typu účtování  | Typ účtování         | Klikněte na **Nový** a přidejte řádek, kde můžete vybrat typ účtování, pro který chcete nastavit výchozí vlastnost řádku. Konkrétní typ účtování lze vybrat pouze jednou v konfiguraci. |
|                        | Vlastnost řádku        | Vyberte výchozí vlastnost řádků pro vybraný typ účtování. Když jsou synchronizovány nové odhady hodin, nové odhady výdajů nebo nové skutečné hodnoty z Project Service Automation, **pole Vlastnost řádku** je nastavena na výchozí hodnotu pro typ účtování. |
| Uzamčení funkce  | Nelze použít       | Vyberte tuto funkci pro zakázání projektů a smluv v aplikaci Finance and Operations, pocházejících z Project Service Automation. Například je možné vypnout možnost upravit smlouvy a projekty, vytvořit struktury rozpisu práce a zadávat časové rozvrhy v aplikaci Finance and Operations. Pole související s účetnictví budou nadále povolena, i v případě, že nejsou k dispozici podle nastavení parametrů. Standardně budou všechny funkce povoleny. |
