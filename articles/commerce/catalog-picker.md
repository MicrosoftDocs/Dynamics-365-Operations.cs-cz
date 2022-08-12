---
title: Modul pro výběr katalogu
description: Tento článek popisuje moduly pro výběr katalogu a popisuje, jak je přidat do webů elektronického obchodování business-to-business (B2B) Microsoft Dynamics 365 Commerce.
author: ashishmsft
ms.date: 07/11/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2022-04-21
ms.openlocfilehash: 642319eea7e40415fd32898f6ec07bfc86f3b1b1
ms.sourcegitcommit: d1491362421bf2fcf72a81dc2dc2d13d3b98122b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/11/2022
ms.locfileid: "9136938"
---
# <a name="catalog-picker-module"></a>Modul pro výběr katalogu

[!include [banner](includes/banner.md)]

Tento článek popisuje moduly pro výběr katalogu a popisuje, jak je přidat do webů elektronického obchodování business-to-business (B2B) Microsoft Dynamics 365 Commerce.

Modul pro výběr katalogu je speciální kontejner, který se používá k výpisu všech katalogů produktů, které jsou k dispozici uživatelům webu B2B pro nákup. Více katalogů je aktuálně podporováno pouze pro B2B weby.

Následující obrázek znázorňuje příklad modulu pro výběr katalogu.

![Příklad modulu pro výběr katalogu, který uvádí tři katalogy produktů.](./media/Catalog-picker-sample.png)

## <a name="add-a-catalog-picker-module-to-your-site"></a>Přidání modulu pro výběr katalogu na web

Chcete-li přidat modul výběru katalogu na svůj web v konfigurátoru webů Commerce, postupujte následujícím způsobem.

### <a name="create-a-catalog-picker-page"></a>Vytvořte stránku pro výběr katalogu

Nejprve vytvořte stránku pro výběr katalogu.

1. Přejděte na **Stránky** a volbou **Nová** vytvořte novou stránku.
1. V dialogovém okně **Vytvořit novou stránku** v části **Název stránky** zadejte **Modul pro výběr katalogu**.
1. V části **Adresa URL stránky** zadejte adresu URL stránky a poté klikněte na tlačítko **Další**.

    ![Dialogové okno Vytvořit novou stránku.](./media/Create-catalog-picker-page.png)

1. V části **Zvolit šablonu** vyberte **Obecný obsah** a pak vyberte **Další**.
1. V části **Zvolit rozvržení** vyberte **Flexibilní rozvržení** a pak vyberte **Další**.
1. V části **Zkontrolovat a dokončit** zkontrolujte konfiguraci stránky. Pokud potřebujete upravit informace o stránce, vyberte **Zpět**. Pokud jsou informace o stránce správné, vyberte **Vytvořit stránku**.
1. V části **Modul pro výběr katalogu** vyberte **Hlavní slot**, vyberte tři tečky (**...**) a vyberte možnost **Přidat modul**.

    ![Přidání modulu do hlavního slotu pod výběrem katalogu.](./media/Author-web-page-catalog-picker-1.png)

1. V dialogovém okně **Vybrat moduly** vyberte modul **Kontejner** a poté klikněte na **OK**.
1. Vyberte slot **Kontejner**, vyberte tři tečky (**...**) a poté vyberte možnost **Přidat modul**.
1. V dialogovém okně **Vybrat moduly** vyberte **Modul pro výběr katalogu** a poté klikněte na tlačítko **OK**.
1. V podokně vlastností **Modul pro výběr katalogu** v části **Nadpis** vyberte **Katalogy** a poté zadejte nadpis pro stránku pro výběr katalogu.
1. V části **Úroveň nadpisu** vyberte úroveň nadpisu a pak vyberte **OK**.
1. Do části **Formátovaný text** zadejte text, který se zobrazí v horní části stránky pro výběr katalogu.
1. Chcete-li vrátit stránku se změnami, vyberte možnost **Uložit**, pak **Dokončit úpravy** a volbou **Publikovat** ji publikujte.

### <a name="add-a-link-on-your-account-page"></a>Přidejte odkaz na stránku svého účtu

Dále přidejte odkaz na stránku pro výběr katalogu na vaší stránce **Můj účet**.

1. Přejděte na **Stránky**, vyhledejte a vyberte stránku **Můj účet** svého webu a poté vyberte **Upravit**.
1. Pod slotem **Hlavní** stránky vyberte slot **Obecná dlaždice účtu**. 
1. V podokně vlastností **Obecná dlaždice účtu** pod **Odkazy** vyberte **Přidat odkaz na akci** a poté vyberte **Odkaz na akci**.
1. V dialogovém okně **Odkaz na akci** pod **Text odkazu** zadejte text odkazu pro odkaz na vaši stránku pro výběr katalogu.
1. V části **Cíl odkazu** vyberte **Přidat odkaz**.
1. V dialogovém okně **Přidat odkaz** vyberte **Vlastní stránka** a poté vyberte **Další**.
1. V části **Název** vyberte stránku pro výběr katalogu, vyberte **Použít** a poté vyberte **OK**.
1. Chcete-li vrátit stránku se změnami, vyberte možnost **Uložit**, pak **Dokončit úpravy** a volbou **Publikovat** ji publikujte.

Následující obrázek ukazuje příklad stránky účtů s odkazem na stránku katalogu.

![Stránka mých účtů s odkazem na katalog.](./media/my-accounts.png)

### <a name="add-a-link-from-the-header"></a>Přidejte odkaz ze záhlaví

Nakonec přidejte odkaz ze záhlaví vašeho webu do svých katalogů.

1. Přejděte na **Fragmenty**, vyhledejte a vyberte fragment záhlaví vašeho webu a poté vyberte **Upravit**.
1. Vyberte slot **Záhlaví**. 
1. V podokně vlastností **Hlavička** pod **Odkazy na můj účet** vyberte **Přidat odkaz na akci** a poté vyberte **Odkaz na akci**.
1. V dialogovém okně **Odkaz na akci** pod **Text odkazu** zadejte text odkazu pro odkaz na vaši stránku pro výběr katalogu.
1. V části **Cíl odkazu** vyberte **Přidat odkaz**.
1. V dialogovém okně **Přidat odkaz** vyberte **Vlastní stránka** a poté vyberte **Další**.
1. V části **Název** vyberte stránku pro výběr katalogu, vyberte **Použít** a poté vyberte **OK**.
1. Chcete-li vrátit fragment záhlaví se změnami, vyberte možnost **Uložit**, pak **Dokončit úpravy** a volbou **Publikovat** jej publikujte.

Následující obrázek ukazuje příklad stránky hlavičky webu e-shopu s odkazem na katalog B2B.

![Záhlaví webu elektronického obchodu s rozevíracím odkazem na katalog.](./media/catalog-in-header.png)


## <a name="additional-resources"></a>Další prostředky 

[Vytváření obchodních katalogů pro B2B weby](catalogs-b2b-sites.md)

[Dopad rozšiřitelnosti u přizpůsobení funkce Katalogy Commerce pro B2B](catalogs-b2b-sites-dev.md)

[Nejčastější dotazy k obchodním katalogům pro B2B](catalogs-b2b-sites-FAQ.md)

[Moduly a stránky správy obchodního vztahu](account-management.md)

[Modul záhlaví](author-header-module.md)
