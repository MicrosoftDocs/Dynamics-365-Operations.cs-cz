---
title: Přidání loga
description: Toto téma popisuje, jak přidat logo na web v řešení Microsoft Dynamics 365 Commerce.
author: bicyclingfool
manager: AnnBe
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 23bac9aae6beb59912bbc9e1f2c6958c007550b0
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/20/2019
ms.locfileid: "2914610"
---
# <a name="add-a-logo"></a>Přidání loga

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Toto téma popisuje, jak přidat logo na web v řešení Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Přehled

Když vytváříte web, jedna z prvních věcí, kterou pravděpodobně uděláte, je přidání loga vaší společnosti nebo značky do záhlaví webu. Online startovací sada řešení Dynamics 365 Commerce poskytuje modul, který tuto úlohu usnadňuje.

Logo můžete přidat přímo do šablony, rozložení nebo stránky. Tímto způsobem můžete snadno změnit logo, které se zobrazí na určitých stránkách nebo skupinách stránek. Toto téma však popisuje nejčastější scénář, ve kterém přidáte logo do fragmentu záhlaví, který lze znovu použít na všech stránkách webu.

## <a name="prerequisites"></a>Předpoklady

Před přidáním loga na všechny stránky webu je nutné tyto úkoly dokončit.

1. Uložte logo do správce digitálních datových zdrojů, ke kterému máte přístup ze stránky **Datové zdroje**.
1. Vytvořte fragment záhlaví. Další informace o vytváření a používání fragmentů naleznete v tématu [Práce s fragmenty](work-with-fragments.md).
1. Zahrňte do šablony fragment záhlaví, který stránky vašeho webu používají pro své možnosti rozložení a modulu. Další informace o šablonách získáte v části [Práce s šablonami](work-with-templates.md).

## <a name="add-a-logo-to-a-header-fragment"></a>Přidání loga do fragmentu záhlaví

Chcete-li přidat logo do fragmentu záhlaví webu, postupujte takto:

1. V navigačním podokně vlevo vyberte **Fragmenty**a pak vyberte fragment záhlaví, který jste vytvořili.
2. Vyberte **Rezervovat**.
3. Rozbalte pozici **Záhlaví** a pozici **Logo**.
4. Vyberte tlačítko se třemi tečkami (**...**) vedle pozice **Logo** a poté vyberte možnost **Přidat modul**.
5. Vyberte modul logo.
6. V podokně vlastností napravo nakonfigurujte modul logo, aby se zobrazilo vaše logo.
7. Uložte fragment záhlaví, vraťte jej se změnami a publikujte.

Po publikování aktualizovaného fragmentu záhlaví budou všechny stránky webu, které používají šablonu obsahující fragment záhlaví, zobrazovat vaše logo.

## <a name="additional-resources"></a>Další zdroje

[Volba motivu webu](select-site-theme.md)

[Práce se soubory přepisu šablon CSS](css-override-files.md)

[Přidání ikony oblíbené položky](add-favicon.md)

[Přidání uvítací zprávy](add-welcome-message.md)

[Přidání oznámení o vlastnických právech](add-copyright-notice.md)

[Přidání jazyků na web](add-languages-to-site.md)

[Přidání kódu skriptu na webové stránky pro podporu telemetrie](add-telemetry.md)

