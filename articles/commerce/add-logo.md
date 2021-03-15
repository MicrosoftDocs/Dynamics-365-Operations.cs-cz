---
title: Přidání loga
description: Toto téma popisuje, jak přidat logo na web v řešení Microsoft Dynamics 365 Commerce.
author: bicyclingfool
manager: AnnBe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 073c3d6f8d5ee88d51efb41f6b9c1a204b82fa12
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4980300"
---
# <a name="add-a-logo"></a>Přidání loga

[!include [banner](includes/banner.md)]

Toto téma popisuje, jak přidat logo na web v řešení Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Přehled

Když vytváříte web, jedna z prvních věcí, kterou pravděpodobně uděláte, je přidání loga vaší společnosti nebo značky do záhlaví webu. Online knihovna modulů Dynamics 365 Commerce poskytuje modul, který tuto úlohu usnadňuje.

Logo můžete přidat přímo do šablony, rozložení nebo stránky. Tímto způsobem můžete snadno změnit logo, které se zobrazí na určitých stránkách nebo skupinách stránek. Toto téma však popisuje nejčastější scénář, ve kterém přidáte logo do fragmentu záhlaví, který lze znovu použít na všech stránkách webu.

## <a name="prerequisites"></a>Předpoklady

Před přidáním loga na všechny stránky webu je nutné tyto úkoly dokončit.

1. Odešlete logo do knihovny médií.
1. Vytvořte fragment záhlaví. Další informace o vytváření a používání fragmentů naleznete v tématu [Práce s fragmenty](work-with-fragments.md).
1. Zahrňte do šablony fragment záhlaví, který stránky vašeho webu používají pro své možnosti rozložení a modulu. Další informace o šablonách získáte v části [Práce s šablonami](work-with-templates.md).

## <a name="add-a-logo-to-a-header-fragment"></a>Přidání loga do fragmentu záhlaví

Chcete-li přidat logo do fragmentu záhlaví webu, postupujte takto:

1. V navigačním podokně nalevo vyberte položku **Fragmenty**.
1. Vyberte záhlaví, které jste vytvořili dříve, a poté vyberte možnost **Upravit**.
1. Rozbalte modul záhlaví.
1. V podokně vlastností modulu záhlaví zadejte obrázek a odkaz na logo. 
1. Uložte fragment záhlaví, dokončete úpravy a publikujte jej.

Po publikování aktualizovaného fragmentu záhlaví budou všechny stránky webu, které používají šablonu obsahující fragment záhlaví, zobrazovat vaše logo.

## <a name="additional-resources"></a>Další zdroje

[Volba motivu webu](select-site-theme.md)

[Práce se soubory přepisu šablon CSS](css-override-files.md)

[Přidání ikony oblíbené položky](add-favicon.md)

[Přidání uvítací zprávy](add-welcome-message.md)

[Přidání oznámení o vlastnických právech](add-copyright-notice.md)

[Přidání jazyků na web](add-languages-to-site.md)

[Přidání kódu skriptu na webové stránky pro podporu telemetrie](add-telemetry.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]