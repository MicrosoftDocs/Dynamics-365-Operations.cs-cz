---
title: Zásady práce ve skladu
description: Zásady práce ve skladu řídí, zda je skladová práce vytvářena skladovými procesy ve výrobě na základě typu pracovního příkazu, skladového místa a produktu.
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkPolicy
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 196561
ms.assetid: cbf48ec6-1836-48d5-ad66-a9b534af1786
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 0710eac8daba7f51f6b5d1522476b812a130960d
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/15/2019
ms.locfileid: "1567025"
---
# <a name="warehouse-work-policies"></a>Zásady práce ve skladu

[!include [banner](../includes/banner.md)]

Zásady práce ve skladu v aplikaci Microsoft Dynamics 365 for Finance and Operations řídí, zda je skladová práce vytvářena skladovými procesy ve výrobě na základě typu pracovního příkazu, skladového místa a produktu.

Tato pracovní zásada řídí, zda je vytvořena práce skladu pro procesy skladu při výrobě. Zásadu práce můžete nastavit použitím kombinace **typů pracovního příkazu**, **skladového místa** a **produktu**. Například produkt L0101 je vykazován jako dokončený na umístění výstupu 001. Hotového výrobek je později spotřebován v jiné výrobní zakázce v umístění výstupu 001. V tomto případě můžete nastavením pracovní zásady zabránit vytvoření práce pro zaskladnění hotových výrobků, když nahlásíte produkt L0101 jako dokončený v umístění výstupu 001. Zásady práce označují individuální entitu, kterou lze popsat pomocí následujících informací:

-   **Název pracovní zásady**(jedinečný identifikátor pracovní zásady)
-   **Typy pracovních činností** a **způsob vytvoření práce**
-   **Skladová místa**
-   **Výrobky**

## <a name="work-order-types"></a>Typy pořadí pracovních činností
Můžete vybrat některý z následujících typů pracovních příkazů:

-   Výdej dokončeného zboží
-   Vyskladnění vedlejšího produktu
-   Výdej suroviny

Pole **Metoda vytváření práce** má hodnotu **Nikdy**. Tato hodnota značí, že pracovní zásada zabrání vytvoření práce ve skladu pro vybraný typ výrobního příkazu.

## <a name="inventory-locations"></a>Skladová místa
Můžete vybrat místo, na které se pracovní zásada vztahuje. Pokud žádné umístění není přidruženo k zásadě práce, zásada práce se nevztahuje na všechny procesy. Na stránce **Umístění** můžete vybrat nebo zrušit výběr zásady práci na určité místo.

## <a name="products"></a>Produkty
Můžete vybrat produkt, na který se pracovní zásada vztahuje. Zásadu práce lze použít pro všechny produkty nebo vybrané produkty.

## <a name="example"></a>Příklad
V následujícím příkladu jsou dvě výrobní zakázky, PRD-001 a PRD-00*2*. Výrobní zakázka PRD-001 má operaci s názvem **Sestavení**, kde produkt SC1 je hlášen jako dokončený v místě O1. Výrobní zakázka PRD-002 má operaci, která se nazývá **Lakování** a spotřebovává produkt SC1 z umístění O1. Výrobní zakázka PRD-002 také spotřebovává suroviny RM1 z umístění O1. RM1 je uložen ve skladu BULK-001 a bude vyskladněno v umístění O1 během práce ve skladu pro výdej surovin. Pro uvolnění výroby PRD-002 je generována práce vyskladnění. 

[![Zásady práce ve skladu](./media/warehouse-work-policies.png)](./media/warehouse-work-policies.png) 

Při plánování konfigurace zásad práce ve skladu pro tento scénář je třeba zvážit následujících informace:

-   Práce ve skladu pro výdej dokončeného zboží není vyžadována, když vykážete produkt SC1 jako dokončený z výrobní zakázky PRD-001 do umístění O1. Důvodem je, že operace **Lakování** pro výrobní zakázku PRD-002 spotřebovává SC1 na stejném místě.
-   Práce ve skladu pro vyzvednutí surovin je požadována pro účely přesunutí surovin RM1 z umístění ve skladu BULK-001 do umístění O1.

Toto je příklad zásad práce, které můžete nastavit na základě těchto důvodů.


|                                       |                                       |
|---------------------------------------|---------------------------------------|
| <strong>Název pracovní zásady</strong><br> | <strong>Typy pořadí pracovních činností</strong><br> |
|         Bez zaskladnění 01     `          |     - Zaskladnění dokončeného výrobku<br>      |
|                                       |    <strong>Umístění</strong><br>     |
|                                       |                 - O1                  |
|                                       |    <strong>Produkty</strong> <br>     |
|                                       |                 - SC1                 |

Následující procedury obsahují podrobné pokyny ke způsobu nastavení zásad pracovního skladu pro tento scénář. Je popsána také ukázka nastavení, která uvádí, jak vykázat výrobní zakázku jako dokončenou v místě, které nemá licenční kód.

## <a name="set-up-a-warehouse-work-policy"></a>Nastavení zásady práce ve skladu
Skladové procesy ne vždy zahrnují skladovou práci. Definováním zásad práce můžete zabránit vytváření práce pro výdej surovin, ale také vyskladnění dokončených výrobků pro sérii produktů v konkrétních umístěních. K vytvoření této procedury jsou použita ukázková data společnosti USMF. 

KROKY (21)

|     |                                                                            |
|-----|----------------------------------------------------------------------------|
| 1.  | Přejděte do nabídky Řízení skladu &gt; Nastavení &gt; Práce &gt; Pracovní zásady.        |
| 2.  | Klikněte na možnost Nový.                                                                 |
| 3.  | Do pole Název pracovní zásady zadejte „Žádné vyskladnění“.                    |
| 4.  | Klepněte na tlačítko Uložit.                                                                |
| 5.  | Klepněte na možnost Přidat.                                                                 |
| 6.  | Označte na seznamu vybraný řádek.                                        |
| 7.  | V poli Typ pořadí pracovních činností vyberte možnost Výdej dokončeného zboží.            |
| 8.  | Klepněte na možnost Přidat.                                                                 |
| 9.  | Označte na seznamu vybraný řádek.                                        |
| 10. | V poli Typ pořadí pracovních činností vyberte Vyskladnění vedlejšího produktu. |
| 11. | Rozbalte oblast Skladová místa.                                    |
| 12. | Klepněte na možnost Přidat.                                                                 |
| 13. | Označte na seznamu vybraný řádek.                                        |
| 14. | V seznamu Sklad zadejte „51“.                                         |
| 15. | V poli Umístění zadejte nebo vyberte hodnotu 001.                              |
| 16. | Rozbalte část Produkty.                                               |
| 17. | Vyberte možnost Vybráno v poli Výběr produktu.                         |
| 18. | Klepněte na možnost Přidat.                                                                 |
| 19. | Označte na seznamu vybraný řádek.                                        |
| 20. | V poli Číslo zboží zadejte nebo vyberte hodnotu L0101.                         |
| 21. | Klepněte na tlačítko Uložit.                                                                |

## <a name="report-a-production-order-as-finished-to-a-location-that-isnt-license-platecontrolled"></a>Vykázání výrobní zakázky jako dokončené v místě, které není řízeno registrační značkou
Tato procedura obsahuje ukázku dokončeného hlášení do skladového místa, které není řízeno registrační značkou. Předpokladem pro tento úkol je příslušné pracovní pravidlo. Předchozí procedura popisovala nastavení pracovních zásad. 

KROKY (25)

<table>
<tbody>
<tr>
<td colspan="3"><strong>Dílčí úkol: Nastavení výstupního umístění.</strong></td>
</tr>
<tr>
<td></td>
<td>1.</td>
<td>Přejděte na nabídce Správa organizace &gt; Zdroje &gt; Skupiny prostředků.</td>
</tr>
<tr>
<td></td>
<td>2.</td>
<td>V seznamu vyberte skupinu prostředků &#39;5102&#39;.</td>
</tr>
<tr>
<td></td>
<td>3.</td>
<td>Klikněte na položku Upravit.</td>
</tr>
<tr>
<td></td>
<td>4.</td>
<td>Do pole Výstupní sklad zadejte &#39;51&#39;.</td>
</tr>
<tr>
<td></td>
<td>5.</td>
<td>Do pole Umístění výstupu zadejte &#39;001&#39;.</td>
</tr>
<tr>
<td></td>
<td>6.</td>
<td>Umístění 001 není umístění řízené registrační značkou. Umístění výstupu bez registrační značky můžete nastavit pouze v případě, že pro umístění existuje příslušné pracovní pravidlo.</td>
</tr>
<tr>
<td colspan="3"><strong>Dílčí úkol: Vytvoření výrobní zakázky a její ohlášení jako dokončené.</strong></td>
</tr>
<tr>
<td></td>
<td>1.</td>
<td>Zavřete stránku.</td>
</tr>
<tr>
<td></td>
<td>2.</td>
<td>Přejděte na Řízení výroby &gt; Výrobní zakázky &gt; Všechny výrobní zakázky.</td>
</tr>
<tr>
<td></td>
<td>3.</td>
<td>Klikněte na možnost Nová výrobní zakázka.</td>
</tr>
<tr>
<td></td>
<td>4.</td>
<td>Do pole Číslo položky zadejte &#39;L0101&#39;.</td>
</tr>
<tr>
<td></td>
<td>5.</td>
<td>Klikněte na položku Vytvořit.</td>
</tr>
<tr>
<td></td>
<td>6.</td>
<td>V podokně akcí klikněte na položku Výrobní zakázka.</td>
</tr>
<tr>
<td></td>
<td>7.</td>
<td>Klepněte na Odhad.</td>
</tr>
<tr>
<td></td>
<td>8.</td>
<td>Klepněte na tlačítko OK.</td>
</tr>
<tr>
<td></td>
<td>9.</td>
<td>Klepněte na tlačítko Start.</td>
</tr>
<tr>
<td></td>
<td>10.</td>
<td>Klikněte na záložku Obecné.</td>
</tr>
<tr>
<td></td>
<td>11.</td>
<td>V poli Automatická spotřeba kusovníku vyberte hodnotu &#39;nikdy&#39;.</td>
</tr>
<tr>
<td></td>
<td>12.</td>
<td>Klikněte na tlačítko OK.</td>
</tr>
<tr>
<td></td>
<td>13.</td>
<td>Klikněte na položku Oznámit jako dokončené.</td>
</tr>
<tr>
<td></td>
<td>14.</td>
<td>Klikněte na záložku Obecné.</td>
</tr>
<tr>
<td></td>
<td>15.</td>
<td>Vyberte možnost Ano v poli Akceptovat chybu.</td>
</tr>
<tr>
<td></td>
<td>16.</td>
<td>Klepněte na tlačítko OK.</td>
</tr>
<tr>
<td></td>
<td>17.</td>
<td>V podokně akcí klikněte na možnost Sklad.</td>
</tr>
<tr>
<td></td>
<td>18.</td>
<td>Klepněte na tlačítko Podrobnosti práce.</td>
</tr>
<tr>
<td></td>
<td>19.</td>
<td>Pokud byla výrobní zakázka ohlášena jako dokončená, žádná práce nebyla pro vyskladnění vytvořena. K tomu dochází, protože jsou definovány zásady práce, které brání generování práce, když je produkt L0101 ohlášen za dokončený v umístění 001.</td>
</tr>
</tbody>
</table>



