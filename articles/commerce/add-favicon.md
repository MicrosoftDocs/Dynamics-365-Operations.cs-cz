---
title: Přidání ikony oblíbené položky
description: Tento článek vysvětluje, jak přidat ikonu oblíbené položky na váš web.
author: bicyclingfool
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 41d6d8f823c7364f9206fd0f7588e35b6f0a018a
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9270430"
---
# <a name="add-a-favicon"></a>Přidání ikony oblíbené položky

[!include [banner](includes/banner.md)]

Tento článek vysvětluje, jak přidat ikonu oblíbené položky na váš web.

Ikona oblíbené položky je malý grafický soubor, který se mimo jiná umsítění zobrazuje na kartě webového prohlížeče, v adresním řádku, v historii procházení a v záložkách nebo oblíbených položkách. Doporučujeme přidat ikonu oblíbené položky na svůj web, protože reprezentuje a posiluje vaši značku a pomáhá rozlišit váš web od jiných webů, které vaši zákazníci navštěvují.

Ačkoli lze na web přidat více ikon oblíbené položky různých velikostí a typů souborů, tento článek ukazuje, jak přidat jednu ikonu oblíbené položky. Stejný proces a umístění se však používají k přidání dalších ikon oblíbené položky.

## <a name="upload-a-favicon-to-your-sites-asset-collection"></a>Odeslání ikony oblíbené položky do kolekce prostředků webu

Chcete-li odeslat ikonu oblíbené položky do kolekce prostředků vašeho webu, postupujte následovně.

1. V levém navigačním podokně vyberte položku **Knihovna médií**.
1. Na panelu příkazů vyberte možnost **Odeslat \> Odeslání mediálních položek**.
1. V okně Průzkumník souborů přejděte na obrazový soubor ikony oblíbené položky, který chcete nahrát, vyberte jej a poté vyberte **Otevřít**.
1. V dialogovém okně **Odeslat mediální položku** zadejte požadovaný název a alternativní text.
1. Chcete-li publikovat obrázky ihned po odeslání, zaškrtněte políčko **Publikovat mediální položky po odeslání**.

    > [!NOTE]
    > Pokud nezaškrtnete políčko **Publikovat prostředky po odeslání**, je nutné vrátit se na stránku **Prostředky** a ručně publikovat ikonu oblíbené položky později.

1. Vyberte **OK**.
1. V podokně vlastností vpravo zkopírujte veřejnou adresu URL ikony oblíbené položky. Tuto adresu URL budete později používat.

## <a name="create-the-html-for-your-favicon"></a>Vytvoření kódu HTML pro ikonu oblíbené položky

Chcete-li vytvořit kód HTML pro ikonu oblíbené položky, použijte následující řetězec HTML. Pro atribut **href** nahraďte **"Public\_URL\_for\_your\_favicon"** veřejnou adresou URL, kterou jste dříve zkopírovali.

`<link rel="shortcut icon" href="Public_URL_for_your_favicon">`

## <a name="create-a-fragment-that-contains-a-metatag-for-your-favicon"></a>Vytvořte fragment, který obsahuje metaznačku pro vaši ikonu oblíbené položky

Chcete-li vytvořit fragment, který obsahuje metaznačku pro ikonu oblíbené položky, postupujte následovně.

1. Přejděte na **Fragmenty** a pak vyberte **Nový**.
1. V dialogovém okně **Nový fragment** vyberte jako modul, na němž je založen fragment **Metaznačky**.
1. Zadejte název fragmentu a poté vyberte **OK**.
1. Ve stromu hierarchie fragmentů vyberte podřízenou položku **Výchozí metaznačky**.
1. V pravém podokně pod **Metaznačky** vyberte **Přidat** a zadejte řetězec HTML, který jste pro oblíbenou položku vytvořili dříve. 
1. Chcete-li publikovat fragment, vyberte možnost **Dokončit úpravy** a volbou **Publikovat**.

## <a name="add-the-metatag-fragment-to-the-html-head-section-of-your-pages"></a>Přidejte fragment s metaznačkami do sekce HTML na vašich stránkách

Pokud chcete přidat fragment metaznačky do části **hlavička** stránek, proveďte následující postup.

1. Přejděte na **Šablony** a otevřete šablonu pro stránky, na které chcete přidat ikonu oblíbené položky. Potom vyberte **Upravit**.
1. Ve stromu hierarchie šablon vyberte tlačítko se třemi tečkami (**...**) napravo od kontejneru **Hlavička HTML** a vyberte **Přidat fragment**.
1. V dialogovém okně **Vybrat fragment** vyberte fragment metaznačky, který jste vytvořili předtím, a pak vyberte tlačítko **OK**.
1. Chcete-li publikovat šablonu, vyberte možnost **Dokončit úpravy** a volbou **Publikovat**.

> [!NOTE]
> Pokud váš web používá více než jednu šablonu, musíte do každé z nich přidat fragment s metaznačkami.

Při náhledu stránek založených na šabloně, do které jste přidali fragment metaznaček, byste nyní měli na kartě prohlížeče vidět ikonu oblíbené položky.

## <a name="additional-resources"></a>Další prostředky

[Přidání loga](add-logo.md)

[Volba motivu webu](select-site-theme.md)

[Práce se soubory přepisu šablon CSS](css-override-files.md)

[Přidání oznámení o vlastnických právech](add-copyright-notice.md)

[Přidání jazyků na web](add-languages-to-site.md)

[Přidání kódu skriptu na webové stránky pro podporu telemetrie](add-telemetry.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
