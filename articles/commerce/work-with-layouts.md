---
title: Práce s přednastavenými rozloženími
description: Toto téma popisuje, jak pracovat s přednastavenými rozloženími v aplikaci Microsoft Dynamics 365 Commerce.
author: phinneyridge
ms.date: 02/03/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 56ad992b6a9fd6fce09cadad70b8098acdc74ac0
ms.sourcegitcommit: 1eef00796f7c5511f432b01800cdf8920992d7d5
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/04/2022
ms.locfileid: "8090838"
---
# <a name="work-with-preset-layouts"></a>Práce s přednastavenými rozloženími

[!include [banner](includes/banner.md)]

Toto téma popisuje, jak pracovat s přednastavenými rozloženími v aplikaci Microsoft Dynamics 365 Commerce.

Před dokončením postupů uvedených v tomto tématu si přečtěte [Přednastavená a vlastní rozložení](templates-layouts-overview.md#preset-and-custom-layouts). Obecný přehled naleznete v tématu [Šablony a rozvržení – přehled](templates-layouts-overview.md).

## <a name="create-a-new-preset-layout"></a>Vytvoření nového přednastaveného rozvržení

Existují dva způsoby vytvoření přednastaveného rozvržení. Existující vlastní rozvržení můžete uložit jako nové přednastavené rozvržení nebo můžete vytvořit přednastavené rozvržení zcela od začátku.

### <a name="create-a-preset-layout-from-an-existing-custom-layout"></a>Vytvoření přednastaveného rozvržení z existujícího vlastního rozložení

Chcete-li vytvořit přednastavené rozvržení z existujícího vlastního rozložení, postupujte následovně.

1. Otevře existující stránku, která aktuálně nepoužívá přednastavené rozvržení a má strukturu modulu, kterou chcete znovu použít pro ostatní stránky na webu.
1. Stránku rezervujte výběrem možnosti **Upravit**.
1. Vyberte **Uložit jako nové rozvržení**. Zobrazí se dialogové okno **Uložit jako nové rozvržení**.
1. Zadejte název a popis vašeho přednastavevného rozložení. Hodnoty, které zadáte, se zobrazí ostatním autorům při vytváření nových stránek z vašeho rozvržení nebo při přepnutí na ni. Zadejte proto hodnoty, které budou užitečné pro autory stránek.
1. Vyberte **OK**.

Přednastavené rozvržení bude nyní k dispozici při vytvoření nových stránek nebo při výběru jiného rozložení pro stránku ve stejné hierarchii šablon.

> [!TIP]
> Chcete-li rychle zjistit, zda je určitá stránka aktuálně svázána s přednastaveným rozvržením, vyberte stránku v zobrazení seznamu stránek a zkontrolujte metadata rozvržení v podokně vlastností vpravo.

### <a name="create-a-new-preset-layout"></a>Vytvoření nového přednastaveného rozvržení

Chcete-li vytvořit přednastavené rozvržení od začátku, postupujte následovně.

1. V navigačním podokně nalevo vyberte položku **Rozvržení**.
1. Vyberte **Nové rozložení**. Zobrazí se dialogové okno **Nové rozvržení**.
1. Vyberte šablonu, kterou chcete použít pro vaše přednastavené rozvržení.
1. Zadejte název a popis vašeho přednastavevného rozložení. Hodnoty, které zadáte, se zobrazí ostatním autorům při vytváření nových stránek z vašeho rozvržení nebo při přepnutí na ni. Zadejte proto hodnoty, které budou užitečné pro autory stránek.
1. Chcete-li vytvořit nové přednastavené rozvržení a otevřít Editor rozložení, klepněte na tlačítko **OK**.
1. V editoru rozložení přidejte a nakonfigurujte moduly pomocí stromu osnovy v levé části a podokna vlastností vpravo. (Proces se podobá procesu přidávání a konfigurování modulů pro šablonu v editoru šablon.) Uspořádání modulů a všechna zamknutá výchozí nastavení se stanou centralizovanou konfigurací modulu pro všechny stránky, které používají toto rozvržení přednastavených položek.

## <a name="modify-a-preset-layout"></a>Úprava přednastaveného rozložení

Chcete-li upravit přednastavené rozvržení, postupujte následovně.

1. V navigačním podokně nalevo vyberte položku **Rozvržení**.
1. V editoru rozvržení vyberte v levém stromu osnovy modul, který chcete upravit. Potom proveďte libovolný z následujících kroků:

    - Chcete-li přesunout modul nahoru nebo dolů uvnitř jeho nadřazeného objektu, vyberte tlačítko se třemi tečkami (**...**) pro modul a pak vyberte **Přesunout nahoru** nebo **Přesunout dolů.**
    - Chcete-li změnit výchozí nastavení modulu, zadejte výchozí hodnoty pomocí podokna vlastností a volitelně je uzamkněte pro všechny podřízené stránky.
    - Chcete-li přidat nové moduly nebo fragmenty do modulů kontejnerů, klepněte na tlačítko se třemi tečkami a poté vyberte možnost **Přidat modul** nebo **Přidat fragment**.
    - Chcete-li odebrat modul z rozvržení, vyberte tlačítko se třemi tečkami a pak vyberte možnost **Odstranit**.

## <a name="change-a-preset-layout-theme"></a>Změna přednastaveného motivu rozložení

Obvyklou praxí je nastavit výchozí motiv pro všechny stránky, které používají přednastavené rozvržení.

Chcete-li nastavit nebo změnit motiv pro všechny podřízené stránky, které používají předdefinované rozvržení, postupujte podle následujících kroků.

1. V editoru rozvržení vyberte v levém stromu osnovy modul kontejneru stránky. (Tento modul je obvykle druhým uzlem a má název **Výchozí stránka**.)
1. V podokně vlastností vpravo vyberte motiv v poli **Motiv**.

## <a name="save-check-in-preview-and-publish-a-preset-layout"></a>Uložení, navrácení se změnami, náhled a publikování přednastaveného rozvržení

Chcete-li uložit a vrátit vaše přednastavené rozvržení se změnami, postupujte podle následujících kroků.

1. V horní části editoru rozvržení vyberte **Uložit**. Uložené změny nemají vliv na navazující stránky, dokud nejsou vráceny se změnami.
1. Vyberte **Dokončit úpravy**. Vaše změny jsou nyní zjistitelné pro navazující workflowy.

Chcete-li zobrazit náhled změn, buď otevřete existující stránku, která používá přednastavené rozvržení, nebo vytvořte novou stránku z rozvržení.

Po zobrazení náhledu změn v rozvržení přednastavených položek můžete publikovat rozvržení na aktivním webu podle jednoho z následujících kroků:

1. Přejděte na **Rozvržení**, vyberte rozvržení a pak vyberte **Publikovat.**
1. Vyberte název rozvržení pro otevření editoru rozložení a pak vyberte **Publikovat**.
1. Publikujte stránku, která odkazuje na nepublikované rozvržení. Rozvržení bude automaticky publikováno.

> [!WARNING]
> Na přednastavená rozvržení lze odkazovat více stránek. Při publikování přednastaveného rozložení si uvědomte, že může být ovlivněno rozvržení více stránek.

## <a name="rename-a-preset-layout"></a>Přejmenování přednastaveného rozložení

Chcete-li přejmenovat přednastavené rozložení v nástroji pro tvorbu webu, postupujte následovně.

1. V levém navigačním podokně vyberte položku **Rozložení**.
1. Vyberte název rozložení, které chcete přejmenovat.
1. Výběrem příkazu **Upravit** začněte úpravu rozložení.
1. V podokně vlastností rozložení vyberte symbol pera vedle názvu rozložení.
1. Podle potřeby upravte název rozložení.
1. Zaškrtnutím políčka potvrďte změnu názvu.
1. Vyberte **Dokončit úpravy**.

## <a name="additional-resources"></a>Další prostředky

[Přehled šablon a rozvržení](templates-layouts-overview.md)

[Práce se šablonami](work-with-templates.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
