---
title: Vytvoření stránek s vlastní odpovědí pro chyby kódu stavu 4xx/5xx
description: Tento článek popisuje, jak vytvořit stránky s vlastní odpovědí pro chyby kódu stavu 4xx a 5xx pomocí nástrojů pro tvorbu obsahu v řešení Microsoft Dynamics 365 Commerce.
author: v-chgri
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 4a3b1762cebc74c1b77f9ca60925608bc966e306
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9276393"
---
# <a name="build-custom-response-pages-for-4xx5xx-status-code-errors"></a>Vytvoření stránek s vlastní odpovědí pro chyby kódu stavu 4xx/5xx

[!include [banner](includes/banner.md)]

Tento článek popisuje, jak vytvořit stránky s vlastní odpovědí pro chyby kódu stavu 4xx a 5xx pomocí nástrojů pro tvorbu obsahu v řešení Microsoft Dynamics 365 Commerce.

Není-li požadavek úspěšný, server vydá odpovědi na chyby kódu stavu HTTP. Kód stavu 404 je zachycen a vrácen v případě, že stránka nebyla nalezena a kód stavu 500 je zachycen a vrácen, pokud dojde k chybě serveru. V Dynamics 365 Commerce mohou uživatelé aplikace vytvářet stránky s vlastními odpovědmi na chyby kódu stavu, které jsou zobrazeny uživatelům.

## <a name="build-a-status-code-error-response-page"></a>Sestavení stránky s odpovědí na chybu kódu stavu

Chcete-li sestavit stránku s odpovědí na chybu kódu stavu, postupujte podle následujících kroků.

1. V upřednostňovaném webovém prohlížeči se přihlaste k řešení Dynamics 365 Commerce. 
1. Vyberte web, pro který chcete vytvořit stránku s odpovědí na chybu kódu stavu 4xx/5xx.

### <a name="build-the-template"></a>Sestavení šablony

Chcete-li sestavit šablonu pro chybu kódu stavu, postupujte podle následujících kroků.

1. Přejděte na **Šablony**.
1. Zvolte **Nová** pro vytvoření šablony stránky.
1. V dialogovém okně **Nová šablona** v části **Název šablony** zadejte název nové šablony a poté klikněte na tlačítko **OK**.
1. Sestavte šablonu na základě struktury, kterou má mít stránka s odpovědí na chybu kódu stavu.
1. Chcete-li vrátit šablonu se změnami, vyberte možnost **Uložit**, pak **Dokončit úpravy** a volbou **Publikovat** ji publikujte. 

### <a name="build-the-status-code-error-response-page"></a>Sestavení stránky s odpovědí na chybu kódu stavu

Chcete-li sestavit stránku s odpovědí na chybu kódu stavu, postupujte podle následujících kroků.

1. Přejít na **Stránky**.
1. Volbou **Nová** vytvořte stránku.
1. V dialogovém okně **Zvolte šablonu** vyberte šablonu a pak v části **Název stránky** zadejte název pro stránku s reakcí na kód chybového stavu. Ponechejte pole **Adresa URL stránky** prázdné.
1. Sestavte stránku.
1. Chcete-li vrátit stránku se změnami, vyberte možnost **Uložit**, pak **Dokončit úpravy** a volbou **Publikovat** ji publikujte.

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


[!INCLUDE[footer-include](../includes/footer-banner.md)]
