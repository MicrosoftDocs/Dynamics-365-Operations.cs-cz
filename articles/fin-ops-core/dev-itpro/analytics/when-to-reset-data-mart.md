---
title: Kdy resetovat datové tržiště
description: V tomto tématu jsou uvedeny okolnosti, které mohou být vylepšeny resetováním datového tržiště, a okolnosti, za kterých je nepravděpodobné, že vám resetování datového tržiště pomůže.
author: jinniew
ms.date: 05/06/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2021-05-06
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: bc2c4ee490f3bebd6e7c91609a06f8dfedfcb628
ms.sourcegitcommit: 5916ea2a94ab9af7aac21f0fc44e194d5ce82917
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/07/2021
ms.locfileid: "5988985"
---
# <a name="when-to-reset-a-data-mart"></a>Kdy resetovat datové tržiště

Resetování datového tržiště může být časově náročné. V závislosti na okolnostech nemusí být tato akce řešením, které je potřeba. V tomto tématu jsou uvedeny okolnosti, které mohou být vylepšeny resetováním datového tržiště, a okolnosti, za kterých je nepravděpodobné, že vám resetování datového tržiště pomůže.  

## <a name="when-do-i-need-to-do-a-data-mart-reset"></a>Kdy je třeba provést reset datového tržiště?
Před resetováním datového tržiště zvažte následující otázky. Odpověď ano na jednu nebo více otázek může znamenat, že vaše organizace může mít prospěch z resetování datového tržiště.

- Byla obnovena databáze aplikací?
- Otevřeli jste incident podpory a technik podpory vám dal pokyn resetovat datové tržiště jako součást kroku odstraňování problémů?
 
## <a name="when-is-it-not-appropriate-to-reset-a-data-mart"></a>Kdy není vhodné resetovat datové tržiště?
Existují okolnosti, kdy nedoporučujeme resetovat datové tržiště. Mezi ně patří následující. 

- Máte problémy s výkonem spojené se synchronizací dat. 
- Pokud máte opakující se vzor pro resetování z některého z následujících důvodů: 
  - **Chybějící data** 
  - **Zaseknutý stav integrace** 
  - **Zastaralé záznamy** - Zastaralé záznamy samy o sobě nutně neospravedlňují resetování datového tržiště. Pokud máte velkou datovou sadu, proces resetování bude nějakou dobu trvat, ale je nepravděpodobné, že by vedl ke zlepšení.
 
## <a name="what-is-a-data-mart-reset"></a>Co je resetování datového tržiště?
- Reset se spustí až po dokončení stávajících úkolů. Tím je zajištěno, že nebudou vložena stará data. V tomto okamžiku se může zobrazit zpráva jako: „Obnovení datového tržiště nebylo možné zpracovat kvůli aktivní úloze. Prosím zkuste to znovu později."
- Reset deaktivuje integrační úlohy a vymaže všechna data datového tržiště. Integrace je znovu povolena.

## <a name="if-i-reset-the-data-mart-will-i-lose-reports-that-ive-already-designed"></a>Pokud resetuji datové tržiště, přijdu o sestavy, které jsem již vytvořil? 
Ne, vaše sestavy jsou uloženy v tabulkách SQL, které nejsou ovlivněny resetem datového tržiště. Pokud se obáváte ztráty jakýchkoli sestav, které jste navrhli, můžete zálohovat návrhy, které nechcete ztratit. Chcete-li je zálohovat, otevřete návrhář sestav a přejděte na **Společnost > Společnosti > Stavební bloky > Export**.
 
## <a name="is-it-necessary-for-all-users-to-exit-the-system-to-reset-the-data-mart"></a>Je nutné, aby všichni uživatelé opustili systém a resetovali datové tržiště?
Ne, uživatelé mohou pokračovat v práci v systému během resetování datového tržiště. Nebudou však mít přístup k žádným sestavám, které byly vytvořeny pomocí nástroje Financial Reporter, dokud nedojde k dokončení resetu. 

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
