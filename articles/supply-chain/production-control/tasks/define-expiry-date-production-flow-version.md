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
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 97ac33d28a49ad0f2a3956ad65b159e4ec4785c7
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4423518"
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

