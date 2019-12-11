---
title: Vytvoření stránek s vlastní odpovědí pro chyby kódu stavu 4xx/5xx
description: Toto téma popisuje, jak vytvořit stránky s vlastní odpovědí pro chyby kódu stavu 4xx a 5xx pomocí nástrojů pro tvorbu obsahu v řešení Microsoft Dynamics 365 Commerce.
author: v-chgri
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: bcceeb1bc68c6432442c863ca06b7ba81d0abed8
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697099"
---
# <a name="build-custom-response-pages-for-4xx5xx-status-code-errors"></a>Vytvoření stránek s vlastní odpovědí pro chyby kódu stavu 4xx/5xx

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Toto téma popisuje, jak vytvořit stránky s vlastní odpovědí pro chyby kódu stavu 4xx a 5xx pomocí nástrojů pro tvorbu obsahu v řešení Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Přehled

Není-li požadavek úspěšný, server vydá odpovědi na chyby kódu stavu HTTP. Kód stavu 404 je zachycen a vrácen v případě, že stránka nebyla nalezena a kód stavu 500 je zachycen a vrácen, pokud dojde k chybě serveru. V Dynamics 365 Commerce mohou uživatelé aplikace vytvářet stránky s vlastními odpovědmi na chyby kódu stavu, které jsou zobrazeny uživatelům.

## <a name="build-a-status-code-error-response-page"></a>Sestavení stránky s odpovědí na chybu kódu stavu

Chcete-li sestavit stránku s odpovědí na chybu kódu stavu, postupujte podle následujících kroků.

1. V upřednostňovaném webovém prohlížeči se přihlaste k řešení Dynamics 365 Commerce. 
1. Vyberte web, pro který chcete vytvořit stránku s odpovědí na chybu kódu stavu 4xx/5xx.

### <a name="build-the-template"></a>Sestavení šablony

Chcete-li sestavit šablonu pro chybu kódu stavu, postupujte podle následujících kroků.

1. Přejít na **Šablony \> Nová šablona**.
1. Pojmenujte novou šablonu.
1. Sestavte šablonu na základě struktury, kterou má mít stránka s odpovědí na chybu kódu stavu.
1. Vraťte šablonu se změnami a publikujte ji.

### <a name="build-the-status-code-error-response-page"></a>Sestavení stránky s odpovědí na chybu kódu stavu

Chcete-li sestavit stránku s odpovědí na chybu kódu stavu, postupujte podle následujících kroků.

1. Přejděte na **Stránky \> Nová stránka**.
1. Pojmenujte stránku s odpovědí na chybu kódu stavu, ale **nenastavujte** pole **Adresa URL**.
1. Sestavte stránku.
1. Vraťte stránku se změnami a publikujte ji.

> [!NOTE]
> Můžete vytvořit samostatné stránky s odpovědí na chyby kódu stavu 4xx a 5xx. Případně můžete pro obě kategorie chyb použít stejnou stránku s obecnou odpovědí na chybu kódu stavu.

### <a name="set-up-a-redirect-for-the-status-code-error-response-page"></a>Nastavení přesměrování na stránku s odpovědí na chybu kódu stavu

Chcete-li nastavit přesměrování pro chybu kódu stavu, postupujte podle následujících kroků.

1. Přejděte na **Adresy URL \> Nová \> Nový alias** a vyberte stránku s odpovědí na chybu kódu stavu, kterou jste vytvořili dříve.
1. V poli **Alias** zadejte buď **výchozí-4xx** nebo **výchozí-5xx** v závislosti na stránce s odpovědí na chybu kódu stavu, pro kterou nastavujete přesměrování. Tyto aliasy musí být publikovány. V opačném případě nebude přesměrování fungovat.
1. Zvolte **OK** pro potvrzení propojení.

> [!NOTE]
> Pokud pro obě kategorie chyb používáte jedinou stránku s odpovědí na chybu kódu stavu, opakujte tento postup a propojte alias jiné kategorie chyb na stejné stránce.

## <a name="additional-resources"></a>Další zdroje

[Práce se šablonami](work-with-templates.md)

[Přidání nové webové stránky](add-new-page.md)

[Vytvoření URL adresy stránky](create-page-url.md)
