---
title: Modul košíku
description: Tohle téma se zabývá moduly košíku a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 12/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: f2db61cf23c217365274297c6e9878a4eb5679f8d9502cb70484372ae43f6b18
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6716877"
---
# <a name="cart-module"></a>Modul košíku

[!include [banner](includes/banner.md)]

Tohle téma se zabývá moduly košíku a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.

Modul košíku zobrazuje položky, které byly přidány do košíku, než odběratel pokračuje v rezervaci. Modul také zobrazuje souhrn objednávky a umožňuje odběrateli použití nebo odebrání propagačních kódů.

Modul košíku podporuje přihlášené uživatele i hosty. Také podporuje odkaz **Zpět na nákupy**. Můžete konfigurovat cestu pro tento odkaz v **Nastavení webu \> Rozšíření \> Cesty**.

Modul košíku vykresluje data založená na ID košíku, což je soubor cookie prohlížeče dostupný v rámci celého webu. 

Následující obrázek ukazuje příklad stránky nákupního košíku na webu Fabrikam.

![Příklad modulu nákupního košíku na webu Fabrikam.](./media/cart2.PNG)

Následující obrázek ukazuje příklad stránky nákupního košíku na webu Fabrikam. V tomto příkladu je za řádkovou položku účtován manipulační poplatek.

![Příklad modulu nákupního košíku s manipulačním poplatkem za řádkovou položku.](./media/ecommerce-handling-fee.png)

## <a name="cart-module-properties-and-slots"></a>Vlastnosti a pozice modulu košíku

| Vlastnost | Hodnoty | popis |
|----------------|--------|-------------|
| Záhlaví | Text a značka nadpisu (**H1**, **H2**, **H3**, **H4**, **H5** nebo **H6**) | Nadpis košíku, jako "Nákupní taška" nebo "Položky v nákupním košíku". |
| Zobrazit chybu vyprodanosti | **Pravda** nebo **nepravda** | Pokud je tato vlastnost nastavena na **Pravda**, na stránce košíku se zobrazí chyby související s akciemi. Doporučujeme nastavit tuto vlastnost na **Pravda** pokud jsou na webu prováděny kontroly zásob. |
| Zobrazit přepravní poplatky u řádkových položek | **Pravda** nebo **nepravda** | Pokud je tato vlastnost nastavena na **Pravda**, řádkové položky košíku zobrazí přepravné, jsou-li tyto informace k dispozici. Tato funkce není v motivu Fabrikam podporována, protože uživatelé vyberou dopravu pouze v pokladně. Tuto funkci však lze zapnout v jiných workflowech, pokud je to možné. |
| Zobrazit dostupné propagační akce| **Pravda** nebo **nepravda** | Pokud je tato vlastnost nastavena na **Pravda**, košík zobrazuje dostupné propagační akce na základě položek v košíku. Tato funkce je k dispozici ve vydání Dynamics 365 Commerce 10.0.16. |

## <a name="modules-that-can-be-used-in-a-cart-module"></a>Moduly, které lze použít v modulu košíku

- **Textový blok** – Tento modul podporuje vlastní zasílání zpráv v modulu košíku. Zprávy řídí systém správy obsahu (CMS). Lze přidat libovolnou zprávu, například „Při problémech s objednávkou volejte 123 456 789“.
- **Volič obchodů** – Tento modul zobrazuje seznam obchodů, které jsou poblíž a kde je položka k výdeji. Umožňuje uživatelům zadat umístění pro hledání obchodů, které jsou v okolí. Další informace o tomto modulu naleznete v tématu [Modul volič obchodů](store-selector.md).

## <a name="module-properties"></a>Vlastnosti modulu

Následující nastavení modulu nákupního košíku lze konfigurovat na **Nastavení webu \> Rozšíření**:

- **Maximální množství** – tato vlastnost se používá k určení maximálního počtu jednotlivých položek, které lze přidat do nákupního košíku. Maloobchodní prodejce může například rozhodnout, že v jedné transakci lze prodávat pouze 10 jednotlivých produktů.
- **Zásoby** – Informace, jak použít nastavení zásob, naleznete v části [Použití nastavení zásob](inventory-settings.md).
- **Zpět k nákupu** – Tato vlastnost se používá k určení trasy pro odkaz **Zpět k nákupu**. Postup lze konfigurovat na úrovni webu a umožnit maloobchodním prodejcům, aby se odběratel mohl vrátit na domovskou stránku nebo na jakoukoli jinou stránku na webu.

> [!IMPORTANT]
> V Dynamics 365 Commerce vydání 10.0.14 a novější jsou položky v košíku agregovány na základě nastavení, která jsou definována v profilu online funkcí pro online obchod v Commerce. Další informace o tom, jak vytvořit profil online funkcí a nastavit vlastnosti, které jsou vyžadovány pro agregaci, najdete v tématu [Vytvořte si online funkční profil](online-functionality-profile.md).

## <a name="commerce-scale-unit-interaction"></a>Interakce Commerce Scale Unit

Modul košíku načítá informace o produktu pomocí rozhraní API Commerce Scale Unit. ID košíku ze souboru cookie prohlížeče se používá k načtení všech informací o produktu z Commerce Scale Unit.

## <a name="add-a-cart-module-to-a-page"></a>Přidání modulu košíku na stránku

Chcete-li přidat modul košíku na novou stránku a nastavit požadované vlastnosti, postupujte následujícím způsobem.

1. Přejděte na **Fragmenty** a volbou **Nový** vytvořte nový fragment.
1. V dialogovém okně **Nový fragment** vyberte modul **Košík**.
1. V části **Název fragmentu** zadejte název pro **Fragment košíku** a poté vyberte **OK**.
1. Vyberte pozici **Nákupní košík**.
1. V podokně vlastností vpravo vyberte symbol tužky, do pole zadejte text záhlaví a poté zaškrtněte symbol zaškrtnutí.
1. V pozici **Nákupní košík** vyberte tři tečky (**...**) a poté vyberte možnost **Přidat modul**.
1. V dialogovém okně **Přidat modul** vyberte modul **Volba obchodu** a poté klikněte na tlačítko **OK**.
1. Chcete-li vrátit fragment se změnami, vyberte možnost **Uložit**, pak **Dokončit úpravy** a volbou **Publikovat** jej publikujte.
1. Přejděte na **Šablony** a poté volbou **Nová** vytvořte novou šablonu.
1. V dialogovém okně **Nová šablona** v části **Název šablony** zadejte název šablony.
1. Ve stromové struktuře vyberte pozici **Obsah**, vyberte tři tečky (**...**) a vyberte možnost **Přidat fragment**.
1. V dialogovém okně **Vybrat fragment** vyberte **Fragment košíku** a pak vyberte tlačítko **OK**.
1. Chcete-li vrátit šablonu se změnami, vyberte možnost **Uložit**, pak **Dokončit úpravy** a volbou **Publikovat** ji publikujte.
1. Přejděte na **Stránky** a volbou **Nová** vytvořte novou stránku.
1. V dialogovém okně **Zvolte šablonu** vyberte šablonu, kterou jste vytvořili, zadejte název stránky a pak vyberte tlačítko **OK**.
1. Vyberte možnost **Uložit** a poté vyberte možnost **Náhled**, chcete-li zobrazit náhled stránky.
1. Chcete-li vrátit stránku se změnami, vyberte možnost **Dokončit úpravy** a volbou **Publikovat** ji publikujte.

## <a name="additional-resources"></a>Další prostředky

[Modul ikony košíku](cart-icon-module.md)

[Modul pokladny](add-checkout-module.md)

[Platební modul](payment-module.md)

[Modul dodací adresy](ship-address-module.md)

[Modul možností doručení](delivery-options-module.md)

[Modul s informacemi o vyzvednutí](pickup-info-module.md)

[Modul podrobností objednávky](order-confirmation-module.md)

[Modul dárkového poukazu](add-giftcard.md)

[Výpočet dostupnosti zásob pro maloobchodní kanály](calculated-inventory-retail-channels.md)

[Vytvoření online funkčního profilu](online-functionality-profile.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]