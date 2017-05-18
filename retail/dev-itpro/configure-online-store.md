---
title: Konfigurovat online obchod
description: "Tento článek poskytuje odkazy na témata, která vám pomohou centrálně konfigurovat a spravovat online obchod z aplikace 365 Microsoft Dynamics for Operations."
author: kfend
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations, Retail
ms.custom: 31541
ms.assetid: 7a25f9b4-a0bb-4e8c-95c0-c0799ec0620d
ms.search.region: Global
ms.author: meeram
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 6b1f91f863c8da35362ebb3036e76aa10d95ba65
ms.openlocfilehash: 563d11fb99c8aebce78f8962dbeeac41fb469041
ms.contentlocale: cs-cz
ms.lasthandoff: 04/26/2017


---

# <a name="configure-an-online-store"></a>Konfigurovat online obchod

[!include[banner](../includes/banner.md)]


Tento článek poskytuje odkazy na témata, která vám pomohou centrálně konfigurovat a spravovat online obchod z aplikace 365 Microsoft Dynamics for Operations.

Témata uvedená v následující tabulce vám pomohou při konfiguraci komponent aplikace Dynamics 365 for Operations - Retail a online obchodu Retail v klientovi aplikace Dynamics 365 for Operations.

## <a name="configure-an-online-store"></a>Konfigurovat online obchod
| Úkol                                                | Podrobnosti                                                                                                                                                                                                                                                                                                                                                   | Témata                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|-----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nakonfigurujte součásti Retail.                        | Nastavte a spravujte informace pro maloobchodní operace. Tyto informace zahrnují obchody, daně, výrobky, dárkové poukazy, promoakce a slevy.                                                                                                                                                                                                          | [Nastavení a udržování maloobchodu](https://technet.microsoft.com/en-us/library/hh597201.aspx) (Obsah webu TechNet pro Microsoft Dynamics AX 2012)                                                                                                                                                                                                                                                                                          |
| Nakonfigurujte hierarchii navigace maloobchodní sítě.    | Vytvořte hierarchii navigačních kategorií maloobchodní sítě pro nastavení struktury kategorie pro produkty, které nabízíte prostřednictvím online obchodu. Definujte hierarchii kategorií a přiřaďte do kategorií produkty, skupiny atributů produktů a hodnoty atributů. Poté přiřaďte hierarchii kategorií k online obchodu.                            | [Nastavení hierarchie maloobchodu](https://technet.microsoft.com/en-us/library/hh580593.aspx) (Obsah webu TechNet pro Microsoft Dynamics AX 2012) [Nastavení atributů a typy atributů](https://technet.microsoft.com/en-us/library/hh227548.aspx) (Obsah webu TechNet pro Microsoft Dynamics AX 2012) [Nastavení maloobchodních skupin atributů](https://technet.microsoft.com/en-us/library/jj728713.aspx) (Obsah webu TechNet pro Microsoft Dynamics AX 2012) |
| Přidejte online obchod do organizační hierarchie. | Než bude možné přiřadit sortiment výrobků, vyřídit vytvořené objednávky online obchodu, nebo generovat sestavy, které obsahují informace z online obchodu, musíte obchod přiřadit do jedné nebo více organizačních hierarchií. Minimálně musíte přiřadit online obchod do organizační hierarchie, která obsahuje sortiment produktů. | [Nastavení online obchodu](https://technet.microsoft.com/en-us/library/jj682095.aspx) (Obsah webu TechNet pro Microsoft Dynamics AX 2012)                                                                                                                                                                                                                                                                                                     |
| Přidejte způsoby dodání do online obchodu.          | Vyberte metody doručení, které nabízí online obchod.                                                                                                                                                                                                                                                                                                 | [Nastavení online obchodu](https://technet.microsoft.com/en-us/library/jj682095.aspx) (Obsah webu TechNet pro Microsoft Dynamics AX 2012)                                                                                                                                                                                                                                                                                                     |
| Namapujte atributy a přidejte metadata.                   | Vyberte možnosti, které určují chování atributů pro každou kategorii nebo produkt kanálu v online obchodě na webu Microsoft SharePoint.                                                                                                                                                                                              | [Nastavení online obchodu](https://technet.microsoft.com/en-us/library/jj682095.aspx) (Obsah webu TechNet pro Microsoft Dynamics AX 2012)                                                                                                                                                                                                                                                                                                     |

## <a name="configure-online-store-products"></a>Konfigurace produktů online obchodu
| Úkol                                 | Podrobnosti                                                                                                                                           | Témata                                                                                                                                                                                                                                                                            |
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Přidejte sortimenty do online obchodu. | Přidejte sortimenty obsahující produkty, které nabízíte v online obchodu.                                                                  | [Nastavení online obchodu](https://technet.microsoft.com/en-us/library/jj682095.aspx) (Obsah webu TechNet pro Microsoft Dynamics AX 2012)                                                                                                                                              |
| Spravujte katalogy.                     | Použijte katalogy produktů k identifikaci produktů, které chcete nabídnout ve svých obchodech.                                                              | [Klíčové úkoly: vytvoření katalogů maloobchodních produktů](https://technet.microsoft.com/en-us/library/jj728712.aspx) (Obsah webu TechNet pro Microsoft Dynamics AX 2012)                                                                                                                           |
| Spravujte ceny.                       | Nastavte a použijte cenové skupiny, které jsou centrálním propojením cen a slev, a kanály, katalogy, umístění a věrnostní programy. | [Nastavení cen pomocí cenových skupin](https://technet.microsoft.com/en-us/library/hh597169.aspx) (Obsah webu TechNet pro Microsoft Dynamics AX 2012) [Nastavení daní](https://technet.microsoft.com/en-us/library/hh580571.aspx) (Obsah webu TechNet pro Microsoft Dynamics AX 2012) |
| Spravujte slevy.                    | Nastavte a spravujte úpravy cen a čtyři druhy slev.                                                                                  | [Nastavení cenových úprav a slev](https://technet.microsoft.com/en-us/library/hh597114.aspx) (Obsah webu TechNet pro Microsoft Dynamics AX 2012)                                                                                                                          |
| Spravujte expediční náklady.             | Nastavte a spravujte expediční náklady, které jsou specifické pro online obchod.                                                                     | [Nastavení expedičních nákladů pro internetové obchody](https://technet.microsoft.com/en-us/library/jj728714.aspx) (Obsah webu TechNet pro Microsoft Dynamics AX 2012)                                                                                                                           |
| Spravujte způsoby dodání.            | Spravujte způsoby dodání, které online obchod nabízí.                                                                                        | [Nastavení způsobů dodání](https://technet.microsoft.com/en-us/library/jj728719.aspx) (Obsah webu TechNet pro Microsoft Dynamics AX 2012)                                                                                                                                            |

## <a name="set-up-data-exchange-between-dynamics-365-for-operations-and-the-online-store"></a>Nastavení výměny dat mezi Dynamics 365 for Operations a online obchodem
| Úkol                                 | Podrobnosti                                                                                                                               | Témata                                                                                                                                                                                                                                                                                  |
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nastavte profily integrace kanálů. | Profily umožňují součástem Retail komunikovat mezi sebou. Před konfigurací nastavení výměny dat nastavte profily. | [Nastavení profilu služby Real-time Service](https://technet.microsoft.com/en-us/library/hh580631.aspx) (Obsah webu TechNet pro Microsoft Dynamics AX 2012) [Nastavení profilu kanálu](https://technet.microsoft.com/en-us/library/jj677402.aspx) (Obsah webu TechNet pro Microsoft Dynamics AX 2012) |

 




