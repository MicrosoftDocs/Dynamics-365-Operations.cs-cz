---
title: Vytvoření webu elektronického obchodu
description: V tomto tématu jsou popsány kroky a informace požadované k vytvoření nového webu e-Commerce v Konfigurátoru webu Dynamics 365 Commerce.
author: bicyclingfool
manager: AnnBe
ms.date: 01/23/2020
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
ms.openlocfilehash: 3d3d8a290f06d9734be21f2d59152acac6857506
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002006"
---
# <a name="create-an-e-commerce-site"></a>Vytvoření webu elektronického obchodu


[!include [banner](includes/banner.md)]

V tomto tématu jsou popsány kroky a informace požadované k vytvoření nového webu e-Commerce v Konfigurátoru webu Dynamics 365 Commerce.

Než začnete vyvíjet svůj web e-Commerce, je nutné nejprve vytvořit nový web v Konfugurátoru webu. 


Chcete-li začít vyvíjet svůj web elektronického obchodu, je nutné nejprve vytvořit nový web ve vývojovém prostředí webu. Než bude možné vytvořit nový web, musí být v aplikaci Commerce vytvořen alespoň jeden online obchod. 


## <a name="set-up-your-site"></a>Zřízení webu

Při zřízení webu postupujte takto.

1. Otevřete prostředí konfigurátoru webu. Odkaz na konfigurátor webu v Microsoft Lifecycle Services (LCS) naleznete na stránce funkcí prostředí pro Commerce.
1. Na domovské stránce vývojového prostředí webu vyberte možnost **Nový web**.
1. V dialogovém okně **Nový web** zadejte následující informace.

| Pole                               | Popis |
|-------------------------------------|-------------|
| Název webu                           | Zadejte zobrazovaný název, který má být použit pro váš web ve vývojovém prostředí webu. Tento název je viditelný pouze ve vývojovém prostředí a nebude zobrazen zákazníkům. |
| Skupina zabezpečení správce webu | Zadejte skupinu zabezpečení Microsoft Azure Active Directory (Azure AD), která spravuje uživatele s rolí správce webu na tomto webu. |
| Výchozí kanál (číslo provozní jednotky) | Vyberte online obchod, který bude pro tento web sloužit jako webová výkladní skříň. Chcete-li, aby váš web elektronického obchodu podporoval více online obchodů, je třeba po zřízení webu k němu přiřadit obchody v **Nastavení webu**. |
| Výchozí jazyk                            | Zadejte výchozí jazyk pro tento online obchod a trh. Online obchod může podporovat více jazyků. Chcete-li podporu více jazyků pro tento online obchod nebo jiný online obchod, můžete tuto podporu nakonfigurovat v **Nastavení webu** po zřízení tohoto webu.  |
| Doména                              | Vyberte název domény, který bude pro tento online obchod sloužit jako doména. Pokud nejsou nakonfigurovány žádné domény pro LCS, můžete toto pole ponechat prázdné. Poté, co je doména konfigurována v LCS, je nutné ji přidat do online obchodu v **Nastavení webu**.  |
| Cesta                              | Pokud web podporuje více jazyků pro daný název domény, použijte pole cesty k vytvoření jedinečné adresy URL webu pro tuto kombinaci domény a jazyka. Pokud je jazyk, který jste zadali v poli **Výchozí jazyk**, jediným jazykem, který bude pro tuto doménu podporován, nebo bude po lokalizaci webu do dalších jazyků i nadále výchozím jazykem, doporučujeme toto pole ponechat prázdné. |


Po vytvoření webu můžete ověřit, zda je přidružen k online obchodu, výběrem karty **Produkty**. Měli byste vidět sortiment produktů, které byly přiděleny online obchodu. Chcete-li přistupovat k přiděleným produktům podle kategorie, můžete použít také rozevírací nabídku v levé horní části stránky.

## <a name="additional-resources"></a>Další zdroje

[Konfigurace názvu domény](configure-your-domain-name.md)

[Nasazení nového webu elektronického obchodu](deploy-ecommerce-site.md)

[Přiřazení online webu ke kanálu](associate-site-online-store.md)

[Správa souborů robots.txt](manage-robots-txt-files.md)

[Nastavení vlastních stránek pro přihlášení uživatelů](custom-pages-user-logins.md)

[Přidání podpory pro síť CDN](add-cdn-support.md)

[Povolení zjišťování obchodu na základě polohy](enable-store-detection.md)
