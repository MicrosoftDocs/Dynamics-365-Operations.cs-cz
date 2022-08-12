---
title: Co je nového nebo změněného v aplikaci Dynamics AX verze 7.0.1 (květen 2016)
description: Tento článek popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics AX verze 7.0.1. Tato verze byla vydána v květnu 2016 a má číslo sestavení 7.0.1265.23014.
author: sericks007
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ROBOTS: NOINDEX, NOFOLLOW
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.custom: 91213
ms.assetid: f0bbc78f-87fc-40e9-b46a-6655893f69be
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 6c65c56dfe5d1e32c440789d207f787169c57269
ms.sourcegitcommit: 873d66c03a51ecb7082e269f30f5f980ccd9307f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/06/2022
ms.locfileid: "9124859"
---
# <a name="whats-new-or-changed-in-dynamics-ax-application-version-701-may-2016"></a>Co je nového nebo změněného v aplikaci Dynamics AX verze 7.0.1 (květen 2016)

[!include [banner](../includes/banner.md)]

Tento článek popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics AX verze 7.0.1. Tato verze byla vydána v květnu 2016 a má číslo sestavení 7.0.1265.23014.

## <a name="electronic-reporting-er"></a>Elektronické výkaznictví (EV)

| Co můžete udělat? | Proč je to důležité? |
|------------------|------------------------|
| Nakonfigurujte běhové dialogové okno pro navrhování sestav elektronické vykazování (EV), aby tak uživatelé mohli vybírat požadované finanční dimenze. | V době spuštění v dialogovém okně pro spuštění sestavy EV mohou uživatelé vybírat z více finančních dimenzí. Zobrazí se podrobné informace o vybraných finančních dimenzích v elektronickém dokumentu, který je generován. |
| Při návrhu sestavy EV nastavte přístup k více finančním dimenzím prostřednictvím jednotného mapování požadovaného zdroje dat. | Stejnou konfiguraci sestavy EV lze použít ke generování elektronických dokumentů, které obsahují transakční data a podrobnosti o finančních dimenzích, bez ohledu na počet finančních dimenzí, které jsou vybrané uživatelem nebo nakonfigurovány pro aktuální právnickou osobu nebo instanci. |
| Nakonfigurujte sestavu EV pro zadávání dat v dynamicky generovaných sloupcích elektronického dokumentu, který je vytvořen ve formátu listu OPENXML. | Zpráva EV umožňuje zadávání dat ve vygenerovaném listu OPENXML pomocí vodorovně replikovaných sloupců. Proto stejnou konfigurací sestavy EV lze znovu použít ke generování elektronických dokumentů, které mají různý počet dynamicky generovaných sloupců. |
| Nakonfigurujte cíle EV tak, aby výstupní výsledek formátu byl směrován do určitého cíle: soubor, e-mail nebo archív (složka Microsoft SharePoint nebo Microsoft Azure Storage). | Dříve se při spuštění konfigurace EV zobrazilo okno se zprávou akce požadující po uživateli akci pro uložení nebo otevření souboru. Pro každou konfiguraci formátu a její komponenty (složku nebo soubor) lze nově předem konfigurovat cíl samostatně. Uživatelé, kterým jsou udělena přístupová práva, mohou také měnit nastavení cíle v době běhu. |

## <a name="pos--microsoft-dynamics-ax-retail"></a>POS – Microsoft Dynamics AX maloobchod

| Co můžete udělat? | Proč je to důležité? |
|------------------|------------------------|
| Použijte prohlížeč Google Chrome. | Prodejci mohou nově spouštět Cloud POS z prohlížeče Chrome a využívat tak všechny funkce, které jsou k dispozici ve verzi Cloud POS pro Microsoft Edge a Internet Explorer. |

## <a name="financial-reporting"></a>Finanční výkaznictví

| Co můžete udělat? | Proč je to důležité? |
|------------------|------------------------|
| Znovu sestavte datové tržiště finančního vykazování. | Při přesunutí databází aplikace Dynamics AX mezi prostředími nebo provádění jiných invazivních změn v prostředí může být potřeba znovu sestavit databázi finančního vykazování. Nyní je dostupný skript prostředí Windows PowerShell, který znovu sestaví databázi za vás. |
| Nově již není možné vybrat možnosti návrháře sestav, které nejsou platné. | Některé možnosti návrháře sestav, které byly použity ve verzích trhu v aplikaci Management Reporter, se na tuto verzi Dynamics AX nevztahují. Tyto možnosti souvisejí s návrhem, výstupem a propojením finanční sestavy. Tyto možnosti byly odebrány z návrháře finančních sestav, aby nedocházelo k chybám uživatele. |

## <a name="financial-management"></a>Správa financí

| Co můžete udělat? | Proč je to důležité? |
|------------------|------------------------|
| Generování souborů kladných plateb pro platby závazků. | Je možné generovat soubory kladných plateb, které pomáhají bankám zabránit podvodným šekům. |

## <a name="warehouse-and-production"></a>Sklad a výroba

<table>
<thead>
<tr>
<th>Co můžete udělat?</th>
<th>Proč je to důležité?</th>
</tr>
</thead>
<tbody>
<tr>
<td>Definujte zásady práce ve skladu, které řídí vytváření práce pro sadu produktů v jednotlivých místech.</td>
<td>Skladové procesy ne vždy zahrnují práci. Použitím nových zásad práce ve skladu můžete zabránit vytváření práce pro výdej surovin, ale také vyskladnění dokončených výrobků pro sérii produktů v konkrétních umístěních.</td>
</tr>
<tr>
<td>Určete, že výstupní místo výroby není řízeno pomocí registračních značek.</td>
<td>Nově můžete určit, že výstupní místo výrobku není řízeno pomocí registračních značek. Tato funkce je například užitečná, pokud nadřazená výrobní objednávka vykazuje dokončené položky přímo do umístění, které slouží jako vstupní místo výroby pro navazující výrobní zakázku.</td>
</tr>
<tr>
<td>Podpora kusovníků, která obsahuje položky s různými dimenzemi produktů pro stejnou položku.</td>
<td>Používáte-li jednu nebo více dimenzí produktu ve výrobě, mohou nastat situace, kde chcete vytvořit položku na základě na různých variant téhož zboží. Další informace naleznete v <a href="/archive/blogs/axmfg/support-for-boms-that-includes-items-with-different-product-dimensions-of-the-same-item">tomto blogu</a>.</td>
</tr>
<tr>
<td>Výrobní zakázky s cyklickými strukturami na první úrovni jejich kusovníků jsou vyloučeny z výpočtu kusovníku pro plánování materiálových zdrojů.</td>
<td>Není možné přiřadit správné úrovně kusovníku k variantám produktů u výrobních zakázek, které způsobují cyklické vztahy v hierarchii kusovníku.</td>
</tr>
<tr>
<td>Výpočet samostatných úrovní kusovníku pro plánování materiálových zdrojů a výpočet nákladů:
<ul>
<li>Pro plánování materiálových zdrojů se úrovně kusovníku počítají v nové tabulce <strong>ReqItemLevel</strong>. Ve výpočtu jsou ignorovány ukončené výrobní zakázky.</li>
<li>Pro výpočet výrobních nákladů se úrovně kusovníku počítají v tabulce <strong>InventTable</strong>. Ve výpočtu jsou zahrnuty ukončené výrobní zakázky.</li>
</ul>
</td>
<td>
<ul>
<li>Při spuštění plánování materiálových zdrojů, jako je například plánování hlavního plánu a rozpad, je nutné přepočítat pouze úrovně kusovníku používané pro plánování materiálových zdrojů. Jinými slovy není třeba vypočítat úrovně kusovníku, které jsou použity pro výpočet výrobních nákladů.</li>
<li>Při spuštění operací pro výpočet nákladů, jako jsou například skladové uzávěrky, je nutné přepočítat pouze úrovně kusovníku používané pro výpočet výrobních nákladů.</li>
</ul>
</td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a>Další prostředky

[Domovská stránka Co je nového a co se změnilo ve finanční a provozní aplikaci](whats-new-changed.md)

[Noví nebo aktualizovaní průvodci úkolem (květen 2016)](new-updated-task-guides-available-may-2016.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
