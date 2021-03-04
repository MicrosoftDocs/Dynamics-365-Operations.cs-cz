---
title: Dokumenty majetku
description: V tomto tématu jsou vysvětleny dokumenty majetku v modulu Správa majetku.
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetObjectDocument
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d1e251dbbede23466109f6219671db7f62d6d420
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4423722"
---
# <a name="asset-documents"></a>Dokumenty majetku

[!include [banner](../../includes/banner.md)]

 

V tomto tématu jsou vysvětleny dokumenty majetku v modulu Správa majetku.

V modulu Správa majetku můžete vytvořit dokumenty tak, že budou automaticky spojeny např. s typy úloh, výrobci majetku, typy majetku nebo majetkem. Tato funkce je užitečná, když jsou vydány aktualizované verze dokumentů. V takovém případě stačí pouze vložit aktualizovaný dokument do standardního umístění, které používáte pro dokumenty Supply Chain Management, a připojit dokument k záznamu o majetku, který jste vytvořili. K aktualizovanému dokumentu pak lze získat přístup z položek nabídky **Všechen majetek**, **Aktivní majetek**, **Můj aktivní majetek** a **Všechny pracovní příkazy** a **Aktivní úlohy pracovního příkazu**. Proces připojování dokumentů k záznamu dokumentu aktiv používá standardní systém zpracování dokumentů.

**Příklad 1:** dokument, který souvisí s typem práce, může popisovat postup pro tento typ úlohy.

**Příklad 2:** dokument, který souvisí s kombinací typu majetku, výrobce a modelu, může být standardní příručkou vybraného modelu výrobce majetku.

## <a name="create-asset-document-relation"></a>Vytvořit vztah dokumentu majetku

1. Vyberte **Správa majetku** \> **Nastavení** \> **Dokumenty majetku**.
2. Vyberte **Nový**, chcete-li vytvořit záznam o dokumentu majetku.
3. V závislosti na tom, jak konkrétní vztah dokumentu chcete, proveďte příslušné výběry v jednom nebo více následujících polí: **Typ majetku**, **Výrobce**, **Model**, **Majetek**, **Kategorie typu práce**, **Typ práce**, **Varianta typu práce** a **Požadavek na práci**. Možnosti, které jsou k dispozici v poli **Varianta typu práce** a **Požadavek na práci** závisejí na vašem výběru v poli **Typ práce**.

    > [!NOTE]
    > Pokud systém vyhledává dokumenty, které by měly souviset s majetkem nebo pracovním příkazem, bude Správa majetku procházet všemi záznamy dokumentu majetku a zkontroluje možnou shodu. Vždy zkontroluje nejdříve nejkonkrétnější kombinaci. Jinými slovy, Správa majetku nejprve zkontroluje shodu v poli **Požadavek na práci**. Pokud není nalezena shoda, zkontroluje shodu v poli **Varianta typu práce**. Pokud není nalezena shoda, zkontroluje shodu v poli **Typ práce** a tak dále. Jak vidíte v rozvržení stránky **Dokumenty práce**, toto chování znamená, že pro nalezení nejspecifičtější kombinace zkontroluje Správa majetku každý záznam zprava doleva pro nalezení shody. Několik dokumentů může souviset s majetkem nebo pracovním příkazem. Úroveň servisu můžete upravit podle požadavku na údržbu nebo podle požadovaného pracovního příkazu.

4. Vyberte **Přílohy**. Zobrazí se standardní stránka **Zpracování dokumentu** zpracování dokumentu.
5. Nastavte doklady nebo poznámky, které by měly být připojeny k záznamu dokumentu majetku. Po připojení dokumentů zobrazí pole **Přílohy** počet dokumentů, které souvisejí se záznamem.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]