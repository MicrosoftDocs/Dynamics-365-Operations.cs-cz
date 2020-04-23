---
title: Definování data vypršení platnosti verze výrobního toku
description: Pro ukončení platnosti a zpracování verze výrobního toku k danému datu nebo naplánování nahrazení aktivní verze novou verzí je nutné nastavit datum vypršení platnosti na verzi.
author: cvocph
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3d942f54b2739f2ca3dcc3e8b8a497166a8edb42
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/02/2020
ms.locfileid: "3212082"
---
# <a name="define-an-expiry-date-for-a-production-flow-version"></a>Definování data vypršení platnosti verze výrobního toku

[!include [banner](../../includes/banner.md)]

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

