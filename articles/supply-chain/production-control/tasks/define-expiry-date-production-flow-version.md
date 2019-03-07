---
title: Definování data vypršení platnosti verze výrobního toku
description: Pro ukončení platnosti a zpracování verze výrobního toku k danému datu nebo naplánování nahrazení aktivní verze novou verzí je nutné nastavit datum vypršení platnosti na verzi.
author: cvocph
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: aa0bde90273f9392a36732ed79afdad2eea8bf86
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "323518"
---
# <a name="define-an-expiry-date-for-a-production-flow-version"></a>Definování data vypršení platnosti verze výrobního toku

[!include [task guide banner](../../includes/task-guide-banner.md)]

Pro ukončení platnosti a zpracování verze výrobního toku k danému datu nebo naplánování nahrazení aktivní verze novou verzí je nutné nastavit datum vypršení platnosti na verzi. Není nutné deaktivovat verzi.


## <a name="set-an-expiration-date-to-end-a-production-flow-version"></a>Nastavení data vypršení platnosti k ukončení verze výrobního toku
1. Přejděte na Řízení výroby > Nastavení > Tok štíhlé výroby > Výrobního toky.
2. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
    * Vyberte výrobní tok, který má verzi, která je již definována.  
3. Klikněte na odkaz na vybraném řádku v seznamu.
4. Klikněte na položku Upravit.
5. Označte v seznamu vybraný řádek.
6. Do pole Datum vypršení platnosti zadejte datum a čas.
    * Pro datum vypršení platnosti se nová verze nespustí nebo neaktivuje. Také již nebude možné vytvořit nebo spustit úlohy pro tento výrobní tok. Dále můžete dokončit zahájené úlohy po datu vypršení platnosti.  

