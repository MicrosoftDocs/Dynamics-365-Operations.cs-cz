---
title: "Co je nového nebo upraveného v aplikaci verze Dynamics AX 7.0.1 (květen 2016)"
description: "Tento článek popisuje funkce, které jsou v aplikaci Microsoft Dynamics AX verze 7.0.1 nové nebo změněné. Tato verze byla vydána v květnu 2016 a má číslo sestavení 7.0.1265.23014."
author: sericks007
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, Developer, IT Pro
ms.search.scope: AX 7.0.0, Operations
ms.custom: 91213
ms.assetid: f0bbc78f-87fc-40e9-b46a-6655893f69be
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: e9752e288eedac687f591275e6a4c71b1e2475f2
ms.contentlocale: cs-cz
ms.lasthandoff: 04/25/2017


---

# <a name="whats-new-or-changed-in-dynamics-ax-application-version-701-may-2016"></a>Co je nového nebo upraveného v aplikaci verze Dynamics AX 7.0.1 (květen 2016)

[!include[banner](../includes/banner.md)]


Tento článek popisuje funkce, které jsou v aplikaci Microsoft Dynamics AX verze 7.0.1 nové nebo změněné. Tato verze byla vydána v květnu 2016 a má číslo sestavení 7.0.1265.23014.

<a name="electronic-reporting-er"></a>Elektronické výkaznictví (EV)
-------------------------

|                                                                                                                                                                                        |                                                                                                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Co můžete udělat?**                                                                                                                                                                   | **Proč je to důležité?**                                                                                                                                                                                                                                                                                                                             |
| Nakonfigurujte běhové dialogové okno pro navrhování sestav elektronické vykazování (EV), aby tak uživatelé mohli vybírat požadované finanční dimenze.                                     | V době spuštění v dialogovém okně pro spuštění sestavy EV mohou uživatelé vybírat z více finančních dimenzí. Zobrazí se podrobné informace o vybraných finančních dimenzích v elektronickém dokumentu, který je generován.                                                                                                                              |
| Při návrhu sestavy EV nastavte přístup k více finančním dimenzím prostřednictvím jednotného mapování požadovaného zdroje dat.                                                  | Stejnou konfiguraci sestavy EV lze použít ke generování elektronických dokumentů, které obsahují transakční data a podrobnosti o finančních dimenzích, bez ohledu na počet finančních dimenzí, které jsou vybrané uživatelem nebo nakonfigurovány pro aktuální právnickou osobu nebo instanci.                                             |
| Nakonfigurujte sestavu EV pro zadávání dat v dynamicky generovaných sloupcích elektronického dokumentu, který je vytvořen ve formátu listu OPENXML.                                           | Zpráva EV umožňuje zadávání dat ve vygenerovaném listu OPENXML pomocí vodorovně replikovaných sloupců. Proto stejnou konfigurací sestavy EV lze znovu použít ke generování elektronických dokumentů, které mají různý počet dynamicky generovaných sloupců.                                                                                 |
| Nakonfigurujte cíle EV tak, aby výstupní výsledek formátu byl směrován do určitého cíle: soubor, e-mail nebo archív (složka Microsoft SharePoint nebo Microsoft Azure Storage). | Dříve se při spuštění konfigurace EV zobrazilo okno se zprávou akce požadující po uživateli akci pro uložení nebo otevření souboru. Pro každou konfiguraci formátu a její komponenty (složku nebo soubor) lze nově předem konfigurovat cíl samostatně. Uživatelé, kterým jsou udělena přístupová práva, mohou také měnit nastavení cíle v době běhu. |

## <a name="pos--microsoft-dynamics-ax-retail"></a>POS – Microsoft Dynamics AX Retail
|                                |                                                                                                                                                                                         |
|--------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Co můžete udělat?**           | **Proč je to důležité?**                                                                                                                                                              |
| Použijte prohlížeč Google Chrome. | Prodejci mohou nově spouštět Cloud POS z prohlížeče Chrome a využívat tak všechny funkce, které jsou k dispozici ve verzi Cloud POS pro Microsoft Edge a Internet Explorer. |

## <a name="financial-reporting"></a>Finanční výkaznictví
|                                                                     |                                                                                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Co můžete udělat?**                                                | **Proč je to důležité?**                                                                                                                                                                                                                                                                                         |
| Znovu sestavte datové tržiště finančního vykazování.                          | Při přesunutí databází aplikace Dynamics AX mezi prostředími nebo provádění jiných invazivních změn v prostředí může být potřeba znovu sestavit databázi finančního vykazování. Nyní je dostupný skript prostředí Windows PowerShell, který znovu sestaví databázi za vás.                                                                |
| Nově již není možné vybrat možnosti návrháře sestav, které nejsou platné. | Některé možnosti návrháře sestav, které byly použity ve verzích trhu v aplikaci Management Reporter, se na tuto verzi Dynamics AX nevztahují. Tyto možnosti souvisejí s návrhem, výstupem a propojením finanční sestavy. Tyto možnosti byly odebrány z návrháře finančních sestav, aby nedocházelo k chybám uživatele. |

## <a name="financial-management"></a>Správa financí
|                                                            |                                                                  |
|------------------------------------------------------------|------------------------------------------------------------------|
| **Co můžete udělat?**                                       | **Proč je to důležité?**                                       |
| Generování souborů kladných plateb pro platby závazků. | Je možné generovat soubory kladných plateb, které pomáhají bankám zabránit podvodným šekům. |

## <a name="warehouse-and-production"></a>Sklad a výroba
|                                                                                                                                                                                                                                                                                                                                                                                         |                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Co můžete udělat?**                                                                                                                                                                                                                                                                                                                                                                    | **Proč je to důležité?**                                                                                                                                                                                                                                                                                                                                                                                                              |
| Definujte zásady práce ve skladu, které řídí vytváření práce pro sadu produktů v jednotlivých místech.                                                                                                                                                                                                                                                                          | Skladové procesy ne vždy zahrnují práci. Použitím nových zásad práce ve skladu můžete zabránit vytváření práce pro výdej surovin, ale také vyskladnění dokončených výrobků pro sérii produktů v konkrétních umístěních.                                                                                                                                                                                                     |
| Určete, že výstupní místo výroby není řízeno pomocí registračních značek.                                                                                                                                                                                                                                                                                                               | Nově můžete určit, že výstupní místo výrobku není řízeno pomocí registračních značek. Tato funkce je například užitečná, pokud nadřazená výrobní objednávka vykazuje dokončené položky přímo do umístění, které slouží jako vstupní místo výroby pro navazující výrobní zakázku.                                                                                                                                                     |
| Podpora kusovníků, která obsahuje položky s různými dimenzemi produktů pro stejnou položku.                                                                                                                                                                                                                                                                                                     | Používáte-li jednu nebo více dimenzí produktu ve výrobě, mohou nastat situace, kde chcete vytvořit položku na základě na různých variant téhož zboží. Další informace naleznete v [tomto blogu](https://blogs.msdn.microsoft.com/axmfg/2015/12/22/support-for-boms-that-includes-items-with-different-product-dimensions-of-the-same-item/).                                                                  |
| Výrobní zakázky s cyklickými strukturami na první úrovni jejich kusovníků jsou vyloučeny z výpočtu kusovníku pro plánování materiálových zdrojů.                                                                                                                                                                                                                                     | Není možné přiřadit správné úrovně kusovníku k variantám produktů u výrobních zakázek, které způsobují cyklické vztahy v hierarchii kusovníku.                                                                                                                                                                                                                                                                                                  |
| Výpočet samostatných úrovní kusovníku pro plánování materiálových zdrojů a výpočet nákladů: • Co se týká plánování materiálových zdrojů, úrovně kusovníku se počítají v nové tabulce **ReqItemLevel**. Ve výpočtu jsou ignorovány ukončené výrobní zakázky. • Pro výpočet výrobních nákladů se úrovně kusovníku počítají v tabulce **InventTable**. Ve výpočtu jsou zahrnuty ukončené výrobní zakázky. | • Při spuštění plánování materiálových zdrojů, jako je například plánování hlavního plánu a rozpad, je nutné přepočítat pouze úrovně kusovníku používané pro plánování materiálových zdrojů. Jinými slovy není třeba vypočítat úrovně kusovníku, které jsou použity pro výpočet výrobních nákladů. • Při spuštění operací pro výpočet nákladů, jako jsou například skladové uzávěrky, je nutné přepočítat pouze úrovně kusovníku používané pro výpočet výrobních nákladů. |

 

<a name="see-also"></a>Viz také
--------

[Novinky a změny](whats-new-changed.md)

[Noví nebo aktualizovaní průvodci úkolem (květen 2016)](new-updated-task-guides-available-may-2016.md)




