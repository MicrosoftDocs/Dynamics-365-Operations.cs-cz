---
title: Nasazení nového klienta elektronického obchodu
description: V tomto tématu je popsán způsob nasazení nového klienta elektronického obchodu pomocí služeb Microsoft Dynamics Lifecycle Services (LCS).
author: psimolin
manager: annbe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: c2632632b9b21dd3a88e9a4df0e65cfd28e579d2
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697444"
---
# <a name="deploy-a-new-e-commerce-tenant"></a>Nasazení nového klienta elektronického obchodu

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

V tomto tématu je popsán způsob nasazení nového webu elektronického obchodu pomocí služeb Microsoft Dynamics Lifecycle Services (LCS).

## <a name="overview"></a>Přehled
    
Microsoft Dynamics Lifecycle Services (LCS) je cloudový pracovní prostor vhodný pro spolupráci, který mohou partneři a zákazníci používat ke správě projektů a prostředí, zobrazování nejnovějších informací o produktech a funkcích Microsoft Dynamics a vytváření, sledování a procházení incidentů podpory. Funkce správy elektronického obchodu jsou integrovány do LCS.

Další informace o LCS naleznete v části [Uživatelská příručka Lifecycle Services](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide).
    
## <a name="get-started"></a>Začínáme

Před inicializací elektronického obchodu je nutné inicializovat projekt, prostředí a Retail Cloud Scale Unit (RCSU). Chcete-li provést inicializaci v LCS, musíte mít oprávnění role vlastníka projektu nebo správce prostředí. Jsou podporovány topologie provozních a sandboxovýchprostředí.

Další informace o prostředích naleznete v části [Plánování prostředí](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/imp-lifecycle/environment-planning). Další informace o RCSU naleznete v tématu [Inicializace Retail Cloud Scale Unit](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/deployment/initialize-retail-channels).

## <a name="initialize-e-commerce"></a>Inicializace elektronického obchodu

Pomocí tohoto postupu můžete inicializovat funkci elektronického obchodu v existujícím prostředí.

Než začnete, ujistěte se, zda jsou k dispozici následující požadované informace:

- Použije se RCSU.
- Skupina zabezpečení Microsoft Azure Active Directory, která bude použita pro systém správce systému elektronického obchodu.
- Skupina zabezpečení Microsoft Azure Active Directory, která bude použita pro moderátory hodnocení a recenzí.
- Domény, které budou přidruženy k prostředí.

Kromě toho můžete shromažďovat následující volitelné informace:

- Informace o Azure AD B2C (business-to-consumer):

    - Název klienta.
    - ID klienta.
    - Vlastní doména přihlašování.
    - Adresa URL odpovědi.
    - ID zásady registrace a přihlášení.
    - ID zásady resetování hesla.
    - ID zásady úpravy profilu.

[!NOTE]
Tyto informace lze přidat později prostřednictvím požadavku na službu.

Po shromáždění požadovaných informací proveďte následující kroky pro inicializaci elektronického obchodu.

1. Přihlaste se do [LCS](https://lcs.dynamics.com).
1. Otevřete projekt obsahující prostředí, ve kterém chcete provést inicializaci elektronického obchodu.
1. V části **Prostředí** vyberte prostředí.
1. V části **Funkce prostředí** vyberte odkaz **Řízení maloobchodu**.
1. Na kartě **Elektronické obchodování** vyberte možnost **Nastavení.** Zobrazí se dialogové okno, v němž je nutné zadat informace, které jsou požadovány pro zřízení.
1. Vyplňte požadované informace a přejděte na další stránku.
1. Na další stránce vyplňte požadované informace a odešlete daný formulář. Vrátíte se na kartu **Elektronické obchodování**, kde by se mělo zobrazit zahájení inicializace.
1. Chcete-li zobrazit stav inicializace, vyberte možnost **Aktualizovat** nebo se za chvíli vraťte na kartu **Elektronické obchodování**.
    
Při inicializaci elektronického obchodu z LCS systém zřizuje několik součástí, které jsou potřebné pro elektronický obchod a přidruží je k prostředí. Po zřízení je karta **Elektronické obchodování** na stránce **Řízení maloobchodu** aktualizována tak, aby reagovala na zřízení. Na stránce jsou zobrazena nejnovější nasazení vlastních nastavení a stav všech dalších probíhajících nasazení. Obsahuje také odkazy na web elektronického obchodu a nástroj pro správu webu elektronického obchodu (nástroj pro vytváření obsahu).

## <a name="access-the-authoring-environment"></a>Přístup do vývojového prostředí

Chcete-li získat přístup do vývojového prostředí , přejděte na kartu **Elektronické obchodování** na stránce **Řízení maloobchodu**. Naleznete zde odkazy na web elektronického obchodu a nástroj pro správu webu.

## <a name="additional-resources"></a>Další zdroje

[Přehled online obchodu](online-store-overview.md)

[Vytvoření webu elektronického obchodu](create-ecommerce-site.md)

[Přiřazení online webu ke kanálu](associate-site-online-store.md)

[Konfigurace názvu domény](configure-your-domain-name.md)

[Přidání podpory pro síť CDN](add-cdn-support.md)

[Povolení zjišťování obchodu na základě polohy](enable-store-detection.md)

[Nastavení vlastních stránek pro přihlášení uživatelů](custom-pages-user-logins.md)
