---
title: Vytvoření webu elektronického obchodu
description: V tomto tématu jsou popsány kroky a informace požadované k vytvoření nového webu elektronického obchodu v Konfigurátoru webu Dynamics 365 Commerce.
author: bicyclingfool
ms.date: 03/04/2022
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 5e451b1c95c3e26d1292e7b8300b62af43c81f2f
ms.sourcegitcommit: b80692c3521dad346c9cbec8ceeb9612e4e07d64
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/05/2022
ms.locfileid: "8388204"
---
# <a name="create-an-e-commerce-site"></a>Vytvoření webu elektronického obchodu

[!include [banner](includes/banner.md)]

V tomto tématu jsou popsány kroky a informace požadované k vytvoření nového webu elektronického obchodu v Konfigurátoru webu Dynamics 365 Commerce.

Když si pořídíte licenci na funkce Dynamics 365 Commerce, bude konfigurátor webu obsahovat startovací web, který můžete použít jako základ pro svůj vlastní web. Pokud však chcete začít úplně od začátku nebo pokud si chcete vytvořit druhý web, budete si muset ve vývojovém prostředí webu založit nový web. 

## <a name="site-creation-prerequisites"></a>Předpoklady pro vytvoření webu

Uživatel konfigurátoru webů musí mít uživatelský účet Microsoft Azure Active Directory (Azure AD), který je součástí skupiny zabezpečení Azure AD přiřazené administrátorům systému elektronického obchodování. Další informace viz [Nasazení nového klienta elektronického obchodu](deploy-ecommerce-site.md).

> [!NOTE]
> Uživatelé Azure AD typu host mohou mít ve vašem klientu Azure AD různá přístupová oprávnění. I když jsou součástí skupiny zabezpečení Azure AD přiřazené administrátorům systému elektronického obchodování, může uživatel typu host potřebovat upravit nastavení oprávnění Azure AD **Externí uživatelé**, aby šlo vytvořit web elektronického obchodu v Commerce. 

Při úpravě nastavení Azure AD **Externí uživatelé** postupujte takto.

1. V portálu Azure přejděte ke klientu Azure AD.
1. Přejděte do nabídky **Uživatelské nastavení \> Externí uživatelé** a vyberte odkaz **Správa nastavení externí spolupráce**. Tím otevřete stránku **Nastavení externí spolupráce**, kde lze nastavit přístup uživatele typu host, nastavení pozvání hostů a omezení spolupráce. 
1. Nastavení externí spolupráce upravte v souladu se zásadami zabezpečení vaší společnosti. 

## <a name="set-up-your-site"></a>Zřízení webu

Při zřízení webu postupujte takto.

1. Otevřete prostředí konfigurátoru webu. Odkaz na konfigurátor webu v Microsoft Lifecycle Services (LCS) naleznete na stránce funkcí prostředí pro Commerce.
1. Na domovské stránce vývojového prostředí webu vyberte možnost **Nový web**.
1. V dialogovém okně **Nový web** zadejte následující informace.

| Pole                               | Popis |
|-------------------------------------|-------------|
| Název webu                           | Zadejte zobrazovaný název, který má být použit pro váš web ve vývojovém prostředí webu. Tento název je viditelný pouze ve vývojovém prostředí a nebude zobrazen zákazníkům. |
| Skupina zabezpečení správce webu | Zadejte skupinu zabezpečení Microsoft Azure Active Directory (Azure AD), která spravuje uživatele s rolí správce webu na tomto webu. |
| Výchozí kanál (číslo provozní jednotky) | Vyberte online obchod, který bude pro tento web sloužit jako webová výkladní skříň. Chcete-li, aby váš web elektronického obchodu podporoval více online obchodů, je třeba po zřízení webu k němu přiřadit obchody v **Nastavení webu**. |
| Výchozí jazyk                            | Zadejte výchozí jazyk pro tento online obchod a trh. Online obchod může podporovat více jazyků. Chcete-li podporu více jazyků pro tento online obchod nebo jiný online obchod, můžete tuto podporu nakonfigurovat v **Nastavení webu** po zřízení tohoto webu.  |
| Doména                              | Vyberte název domény, který bude pro tento online obchod sloužit jako doména. Pokud nejsou nakonfigurovány žádné domény pro LCS, můžete toto pole ponechat prázdné. Poté, co je doména konfigurována v LCS, je nutné ji přidat do online obchodu v **Nastavení webu**.  |
| Cesta                              | Pokud web podporuje více jazyků pro daný název domény, použijte pole cesty k vytvoření jedinečné adresy URL webu pro tuto kombinaci domény a jazyka. Pokud je jazyk, který jste zadali v poli **Výchozí jazyk**, jediným jazykem, který bude pro tuto doménu podporován, nebo bude po lokalizaci webu do dalších jazyků i nadále výchozím jazykem, doporučujeme toto pole ponechat prázdné. |

Po vytvoření webu můžete ověřit, zda je přidružen k online obchodu, výběrem karty **Produkty**. Měli byste vidět sortiment produktů, které byly přiděleny online obchodu. Chcete-li přistupovat k přiděleným produktům podle kategorie, můžete použít také rozevírací nabídku v levé horní části stránky.

## <a name="rename-your-site"></a>Přejmenování webu

Chcete-li na web přejmenovat v konfigurátoru webů, postupujte podle následujících kroků.

1. Chcete-li otevřít zobrazení seznamu webů, vyberte **Přepínač webů** v pravém horním rohu a poté vyberte **Spravovat weby**. 
1. Zaškrtněte políčko vedle webu, který chcete přejmenovat, a poté vyberte **Přejmenovat** na příkazovém řádku.
1. V dialogovém okně **Nový název webu** zadejte nový název webu a poté klikněte na tlačítko **OK**. Seznam webů se aktualizuje a zobrazí nový název webu.

## <a name="additional-resources"></a>Další prostředky

[Konfigurace názvu domény](configure-your-domain-name.md)

[Nasazení nového klienta elektronického obchodu](deploy-ecommerce-site.md)

[Přidružení webu Dynamics 365 Commerce k online kanálu](associate-site-online-store.md)

[Správa souborů robots.txt](manage-robots-txt-files.md)

[Hromadné odeslání přesměrování URL adresy](upload-bulk-redirects.md)

[Nastavení klienta B2C v Commerce](set-up-B2C-tenant.md)

[Nastavení vlastních stránek pro přihlášení uživatelů](custom-pages-user-logins.md)

[Konfigurace několika klientů B2C v prostředí Commerce](configure-multi-B2C-tenants.md)

[Přidání podpory pro síť CDN](add-cdn-support.md)

[Povolení zjišťování obchodu na základě polohy](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
