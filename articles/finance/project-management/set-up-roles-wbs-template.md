---
title: Vytváření rolí pro šablony strukturovaného rozpisu prací
description: Toto téma poskytuje informace o nastavení informací o rolích v šablonách strukturovaného rozpisu prací.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5dfb429eae933ba4d687ec4cbd417d2f78308e47
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760496"
---
# <a name="set-up-roles-on-work-breakdown-structure-templates"></a>Vytváření rolí pro šablony strukturovaného rozpisu prací

[!include [banner](../includes/banner.md)]

Vedoucí projektu může nastavit šablony strukturovaného rozpisu prací (WBS), které později použijí při vytváření struktury WBS pro nové projekty. Vedoucí projektu nyní může při vytváření šablony přidat role. Pomocí následujícího postupu se přiřadí role k šabloně WBS. 

1. Vyberte **Řízení a účetnictví projektů** > **Nastavení** > **Projekty** > **Šablony strukturovaného rozpisu prací**.
2. Vyberte **Podrobnosti** u vybrané šablony WBS.
3. Vyberte úkol v seznamu a pak v poli **Role** vyberte roli pro přiřazení k úloze.

## <a name="work-with-a-wbs"></a>Práce se strukturou WBS

Můžete vytvořit novou strukturu WBS, nebo můžete zkopírovat strukturu WBS z existující šablony WBS. Manažer projektu může snadno spravovat prostředky přiřazením rolí k novým úkolům v rámci WBS. Role lze nahradit buď po pořízení zdroje, nebo po určení zdroje, který potvrdil práci na úkolu. Tato možnost umožňuje vedoucím projektu provádět následující úkoly:

- Určit počet prostředků, které jsou požadovány pro balíky práce WBS.
- Odhadovat náklady na projekt.
- Určovat předběžný rozpočet.
- Odhadovat dobu trvání aktivity na základě rolí a zdrojů.
- Vyvíjet některé plány pro vedení projektu, které jsou založené na informacích o projektu.

Další možnosti byly přidány do struktury WBS a umožňují lepší využití přidělování prostředků.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Možnost</th>
<th>Popis</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Přiřazení prostředků</td>
<td>Úlohy spojené se strukturou WBS viz přidělené prostředky, data, počty hodin a typ rezervace.</td>
</tr>
<tr class="even">
<td>Automaticky generovat tým</td>
<td>Automaticky přidělíte plánované prostředky pomocí rolí, které jsou přidruženy k úkolu. Aplikace Finance automaticky navrhuje plánované prostředky použitím analýzy kritérií s více rozhodnutími založené na rolích. Po nastavení rolí a úsilí (hodiny) pro úkoly ve struktuře WBS a po vydání struktury vyberte <strong>Automaticky generovat tým</strong>. Požadovaný počet plánovaných prostředků je přidán do struktury WBS a na kartu <strong>Plánování projektu a týmu</strong>.</td>
</tr>
<tr class="odd">
<td>Prostředek (rozevírací seznam)</td>
<td>Na stránce <strong>Spuštění přiřazení zdrojů </strong>můžete vybrat prostředky, které chcete závazně nebo nezávazně rezervovat podle zadaného trvání. Můžete upravit nastavení zobrazení a prohlédnout si trvání aktivit prostředku. Pomocí následujících možností můžete vybrat a přiřadit prostředky na úrovni balíčku práce:
<ul>
<li><strong>Přijmout</strong> – potvrdit změny u prostředku, který je přiřazen k úkolu.</li>
<li><strong>Storno</strong> – zrušit změny u prostředku, který je přiřazen k úkolu.</li>
<li><strong>Automaticky přiřadit</strong> – Dostupný personální zdroj s odpovídající rolí je automaticky vybrán a přiřazen ke zvolenému úkolu.</li>
</ul></td>
</tr>
</tbody>
</table>

1. Na stránce **Všechny projekty** vyberte projekt **Upgrade XYZ fáze 2**.
2. Vyberte **Plán** > **Aktivity** > **Strukturovaný rozpis prací**.
3. Vyberte **Nový** a přidejte tak následující činnosti první úrovně do struktury WBS:

    - Inicializace
    - Plánování
    - Zpracování
    - Sledování a řízení
    - Zavřít

4. Nastavte data a úsilí (v hodinách), jak je uvedeno na následujícím obrázku.

    [![Nastavení dat a úsilí](./media/projectresourcing10.jpg)](./media/projectresourcing10.jpg)

5. Vyberte řádek úlohy **Inicializace** a v poli **Role** vyberte **Vyšší manažer projektu**.
6. Zvolte **Publikovat**.
7. Na stejném řádku v poli **Zdroj** vyberte **Daniel Goldschmidt** a potom vyberte **Přijmout**.
8. Vyberte řádek úlohy **Plánování** a v poli **Role** vyberte **Obchodní analytik**.
9. Vyberte **Publikovat** a poté vyberte **Automaticky generovat tým**.
10. V otevřeném okně se zprávou vyberte **Ano**.
11. V poli **Prostředek** zkontrolujte, zda je hodnota **Obchodní analytik 1**.
12. U prostředku **Obchodní analytik 1** spusťte vyhledávání a vyberte **Spustit formulář přiřazení prostředku**. Pak vyberte pracovníka pro úlohu.
13. Vyberte**Předběžně přiřadit** &gt; **Plná kapacita**.

    > [!NOTE] 
    > Neobdržíte upozornění, že vybraný prostředek je nyní „2“, protože počet prostředků zůstává „1“.

14. Na stránce **Strukturovaný rozpis prací** ověřte přiřazení prostředku ve struktuře WBS a vyberte **Uložit**.
