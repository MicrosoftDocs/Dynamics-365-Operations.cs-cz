---
title: Workflowy zásobování a zdrojů
description: Některé organizace vyžadují, aby nákupní žádanky a nákupní objednávky byly schváleny uživatelem, který se liší od osoby, která transakci vytvořila. Workflow můžete vytvořit za účelem nastavení schvalovacího procesu.
author: Henrikan
ms.date: 12/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WorkflowTableListPageRnr
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2074
ms.assetid: e54a1d59-b9fb-421b-821d-01f32878aa9b
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a819093d9ee6f999e637281e54905968fe361566
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/29/2021
ms.locfileid: "7575529"
---
# <a name="procurement-and-sourcing-workflows"></a>Workflowy zásobování a zdrojů

[!include [banner](../includes/banner.md)]

Některé organizace vyžadují, aby nákupní žádanky a nákupní objednávky byly schváleny uživatelem, který se liší od osoby, která transakci vytvořila. Workflow můžete vytvořit za účelem nastavení schvalovacího procesu.

Workflow představuje obchodní proces. Definuje, jakým způsobem dokument prochází systémem a určuje, kdo musí zpracovat úkol nebo schválit dokument. Používání systému workflowu v organizaci má několik výhod:

- **Konzistentní procesy:** Můžete definovat schvalovací proces pro specifické dokumenty, například nákupní požadavky a vyúčtování výdajů. Používáním systému workflowu lze zajistit, aby byly dokumenty zpracovávány a schvalovány jednotným a efektivním způsobem.
- **Viditelnost procesů:** –Můžete sledovat stav, historii a výkonnostní metriku konkrétní instance workflowu. To umožňuje určit, zda je potřeba provést změny workflowu ke zvýšení efektivity.
- **Centralizovaný seznam pracovních položek**: Uživatelé mohou zobrazit centralizovaný seznam pracovních položek, když chtějí zobrazit úkoly workflowu a schválení, která jsou k nim přiřazená v rámci všech workflowů, kterých se účastní. To je k dispozici na stránce Pracovní položky.

## <a name="the-types-of-workflows-that-you-can-create"></a> Typy workflowů, které můžete vytvářet

Následující typy workflowu jsou k dispozici pro modul Zásobování a zdroje.

| Typ | Tento typ slouží k: |
|---|---|
| Kontrola nákupních žádanek | Vytvořte kontrolu a workflow schvalování pro nákupní požadavky |
| Kontrola řádku nákupní žádanky | Vytvořte kontrolu a workflow schvalování pro řádky nákupního požadavku. |
| Workflow nákupní objednávky | Vytváření workflowů kontroly a schvalování pro nákupní objednávky. |
| Workflow řádku nákupní objednávky | Vytváření workflowů kontroly a schvalování pro řádky nákupní objednávky. |
| Workflow přihlášky přidání dodavatele | Vytvořte kontrolu a workflow schvalování pro přidání nových dodavatelů prostřednictvím oslovení dodavatele. |

> [!IMPORTANT]
> Když přidáváte nový pracovní postup, mohou se vám také zobrazit následující zastaralé pracovní postupy uvedené v dialogovém okně **Vytvořit pracovní postup** . Ty se vztahují k funkci *potvrzení o přijetí*, která byla k dispozici v [Dynamics AX 2012](/dynamicsax-2012/appuser-itpro/set-up-procurement-and-sourcing-workflows), ale která je nyní zastaralá. Tyto pracovní postupy nejsou aktuálně podporovány.
> 
> - Workflow oznámení data dodání
> - Workflow oznámení přijaté faktury
> - Příjemka produktu v oznámení workflowu selhala.
> - Workflow oznámení o odmítnutí nepotvrzené příjemky produktu

## <a name="creating-a-workflow"></a>Vytvoření workflowu

Chcete-li vytvořit workflow, přejděte do nabídky Zásobování a zdroje &gt; Nastavení &gt; Workflowy zásobování a zdrojů a vytvořte nový workflow tak, že vyberete požadovaný typ workflowu k vytvoření. 

Na plátně workflowu můžete přetahovat prvky workflowu do návrháře a spojovat prvky do toku Prvky workflowu je třeba konfigurovat. Co se týká prvků workflowu pro schválení a úlohy, můžete nastavit, který účastník má provést akci.

## <a name="types-of-participants"></a>Typy účastníků

Můžete přiřadit krok schválení k následujícím skupinám účastníků.

| Skupina uživatelů | Popis |
|---|---|
| Účastník | Přiřaďte krok schválení členům skupiny nebo role. |
| Hierarchie | Přiřaďte krok schválení k uživatelům v určité organizační hierarchii. |
| Uživatel workflowu | Přiřaďte krok schválení uživatelům tohoto pracovního postupu. |
| Fronta | Přiřaďte kroku schválení frontě pracovních položek. |
| Uživatel | Přiřaďte krok schválení konkrétním uživatelům. |

## <a name="additional-resources"></a>Další zdroje

- [Definování workflowů pracovních postupů pro nákupní žádanky](https://www.microsoft.com/download/details.aspx?id=101821)
- [Workflow nákupní žádanky](purchase-requisitions-workflow.md)
- [Nábor dodavatelů](vendor-onboarding.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]