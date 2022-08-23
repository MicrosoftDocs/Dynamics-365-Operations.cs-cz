---
title: Modul rychlého zobrazení
description: Tento článek se zabývá moduly rychlého zobrazení a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 05/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2020-01-08
ms.dyn365.ops.version: Release 10.0.17
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 16f4b0aad803434f10a1c0ab8375552772ee534a
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9286857"
---
# <a name="quick-view-module"></a>Modul rychlého zobrazení

[!include [banner](includes/banner.md)]

Tento článek se zabývá moduly rychlého zobrazení a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.

Modul rychlého zobrazení umožňuje uživatelům rychle zobrazit informace o produktu při procházení produktů na stránce seznamu a přidat jeden nebo více produktů do košíku ze stránky seznamu, aniž by museli přejít na stránku s podrobnostmi o produktu (PDP). Modul rychlého zobrazení poskytuje přehled informací o produktu, které uživatelé potřebují, aby se mohli rozhodnout „přidat do košíku“. Poskytuje také odkaz na PDP, aby si uživatelé mohli prohlédnout další podrobnosti o produktu a možnosti nákupu.

Modul rychlého zobrazení podporuje moduly [kolekce produktů](product-collection-module-overview.md) a [výsledky vyhledávání](search-result-module.md).

> [!IMPORTANT]
> Modul rychlého zobrazení je k dispozici od verze Commerce verze 10.0.17.

Následující obrázek ukazuje příklad modulu rychlého zobrazení na stránce se seznamem produktů.

![Příklad modulu rychlého zobrazení na stránce se seznamem produktů.](./media/ecommerce-quickview.PNG)

## <a name="module-properties"></a>Vlastnosti modulu

Modul rychlého zobrazení podporuje některé ze stejných funkcí jako modul buy boxu. Vlastnosti modulu rychlého zobrazení se tedy podobají vlastnostem modulu buy boxu.

| Vlastnost | Hodnoty | popis |
|----------------|--------|-------------|
| Značka záhlaví | **H1**, **H2**, **H3**, **H4**, **H5** nebo **H6** | Tato vlastnost definuje značku nadpisu produktu. Je-li modul rychlého zobrazení v horní části stránky, měla by být tato vlastnost nastavena na **H1**, aby vyhovovala standardům usnadnění. |
| Povolit vlastní cenu | **Pravda** nebo **nepravda** | Pokud je tato vlastnost nastavena na **True**, může uživatel zadat vlastní cenu. |
| Minimální cena | Celé číslo | Tato vlastnost je použitelná pouze v případě, že je vlastnost **Povolit vlastní cenu** nastavena na **True**. Definuje minimální cenu, kterou může uživatel zadat (například 1 USD). |
| Maximální cena | Celé číslo | Tato vlastnost je použitelná pouze v případě, že je vlastnost **Povolit vlastní cenu** nastavena na **True**. Definuje maximální cenu, kterou může uživatel zadat (například 1 000 USD). |

## <a name="commerce-site-builder-settings"></a>Nastavení konfigurátoru webů Commerce

Stejně jako modul buy boxu, modul rychlého zobrazení respektuje nastavení na **Nastavení webu \> Rozšíření \> Přidat produkt do košíku**. Nastavení **Přejít na stránku košíku** je však ignorováno, protože je v rozporu s účelem modulu rychlého zobrazení, kterým je umožnit uživatelům procházet více produktů na stránce seznamu a přidávat je do košíku, aniž by se vzdalovali od stránky seznamu.

## <a name="add-a-quick-view-module-to-a-product-collection-module"></a>Přidání modulu rychlého zobrazení do modulu kolekce produktů

Modul rychlého zobrazení lze přidat do modulů kolekce produktů a výsledky vyhledávání.

Chcete-li přidat modul rychlého zobrazení do modulu kolekce produktů v konfigurátoru webů Commerce, postupujte následujícím způsobem.

1. Přejděte na **Stránky** a poté vyberte domovskou stránku webu Fabrikam.
1. Přejděte na libovolný modul **Kolekce produktů** na domovské stránce, vyberte tři tečky (**...**) a poté vyberte **Přidat modul**.
1. V dialogovém okně **Vyberte moduly** vyberte modul **Rychlé zobrazení** a poté klikněte na tlačítko **OK**.
1. V podokně vlastností modulu **Rychlé zobrazení**, vyberte **Nadpis**. V dialogovém okně **Nadpis**, nastavte pole **Úroveň nadpisu** na **H2** a potom vyberte **OK**.
1. Chcete-li vrátit stránku se změnami, vyberte možnost **Uložit**, pak **Dokončit úpravy** a volbou **Publikovat** ji publikujte.

## <a name="additional-resources"></a>Další prostředky

[Přehled knihovny modulů](starter-kit-overview.md)

[Modul buy boxu](add-buy-box.md)

[Modul kolekce produktů](product-collection-module-overview.md)

[Modul výsledků hledání](search-result-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
