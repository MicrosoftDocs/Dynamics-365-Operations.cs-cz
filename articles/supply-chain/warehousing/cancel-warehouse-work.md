---
title: Zrušení práce skladu pro zpracování výjimek
description: V tomto tématu je popsána funkce zrušení práce, která vedoucímu skladu umožňuje blokovat práci.
author: omulvad
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSTroubIeshootingSeIfService
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2019-10-1
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: cb725885fb48293a08915f13a4fb14085e930444
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/02/2020
ms.locfileid: "3205798"
---
# <a name="cancel-warehouse-work-for-exception-handling"></a>Zrušení práce skladu pro zpracování výjimek

[!include [banner](../includes/banner.md)]

Funkce Zrušit práci v aplikaci Microsoft Dynamics 365 Supply Chain Management umožňuje správci zrušit určitou aktuálně probíhající práci skladu, ale je blokována systémem nebo ji nelze dokončit z důvodu výjimečných okolností. Tato funkce je atraktivní a zabezpečená alternativa se správnými opravnými skripty SQL, které opravují nekonzistentní data. Avšak vzhledem k tomu, že tyto skripty jsou obvykle vyžadovány odborníky z oblasti IT, funkce zrušení práce mohou používat uživatelé ve společnosti, kteří mají oprávnění správce.

K funkci Zrušit práci můžete přejít klknutím na položky **Řízení skladu** \> **Pravidelné úkoly** \> **Vymazat \> Zrušit práci**. V dialogovém okně **Zrušit práci** zadejte ID práce pro práci, kterou chcete zrušit, a poté klikněte na tlačítko **OK**.

## <a name="warehouse-work-that-can-be-canceled"></a>Skladová práce, kterou lze zrušit

Během operací vyskladnění může pracovník narazit na situace, kdy zaregistroval množství, která byla vydána z místa uložení do svého umístění uživatele, ale nemohl registrovat operaci výběru. Nekonzistentní data skladu jsou často, ale ne vždy, důvodem zablokování práce.

Na rozdíl od běžné funkce zrušení, ke které lze získat přístup pomocí tlačítka **zrušit** v záhlaví práce, nemusí funkce zrušení práce vyžadovat, aby byl poslední dokončený řádek práce řádkem **vyzvednout**. Jinými slovy, pro funkci zrušení práce lze spustit logiku zrušení i v případě, že se množství položky na řádku práce nachází v umístění uživatele.

> [!NOTE]
> V případě práce, která musí být zrušena z provozních důvodů, musí uživatelé skladu nadále používat pravidelné funkce zrušení na stránce práce.

Pomocí funkce Zrušit práci lze zrušit pouze práci typu **Prodej**, **Problém s převodem**, **Vyzvednutí surovin** nebo **Doplnění**. Logika zrušení nebude spuštěna pro zmrazenou práci výběru surovin nebo práci, kterou lze zrušit pomocí běžné funkce zrušení (Další informace naleznete v předchozí poznámce).

Chcete-li odblokovat práci, systém zruší všechny zbývající řádky práce a opraví data skladu přidružená k ID práce, kterou daný uživatel určil. Všechny běžné operace zpracování skladu, které zahrnují ovlivněné množství zboží, mohou být opět obnoveny.

Chcete-li po zrušení práce vložit ovlivněnou položku do určitého umístění, musí uživatel použít operaci pohybu zásob nebo úpravy množství v mobilním zařízení.
