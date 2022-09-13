---
title: Zrušení práce skladu pro zpracování výjimek
description: V tomto článku je popsána funkce zrušení práce, která vedoucímu skladu umožňuje blokovat práci.
author: Mirzaab
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSTroubIeshootingSeIfService, WHSTroubleshootingSelfService
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2019-10-1
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: b1e2036e4e7a8a47d6df029f285df7aca0fa74e6
ms.sourcegitcommit: 0220be95c007c77ba3b73fed8ac68a3d72dc2884
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/02/2022
ms.locfileid: "9403656"
---
# <a name="cancel-warehouse-work-for-exception-handling"></a>Zrušení práce skladu pro zpracování výjimek

[!include [banner](../includes/banner.md)]

Funkce Zrušit práci v aplikaci Microsoft Dynamics 365 Supply Chain Management umožňuje správci zrušit určitou aktuálně probíhající práci skladu, ale je blokována systémem nebo ji nelze dokončit z důvodu výjimečných okolností. Tato funkce je atraktivní a zabezpečená alternativa se správnými opravnými skripty SQL, které opravují nekonzistentní data. Avšak vzhledem k tomu, že tyto skripty jsou obvykle vyžadovány odborníky z oblasti IT, funkce zrušení práce mohou používat uživatelé ve společnosti, kteří mají oprávnění správce.

K funkci Zrušit práci můžete přejít kliknutím na položky **Řízení skladu** \> **Pravidelné úkoly** \> **Vymazat \> Zrušit práci**. V dialogovém okně **Zrušit práci** zadejte ID práce pro práci, kterou chcete zrušit, a poté klikněte na tlačítko **OK**.

## <a name="warehouse-work-that-can-be-canceled"></a>Skladová práce, kterou lze zrušit

Během operací vyskladnění může pracovník narazit na situace, kdy zaregistroval množství, která byla vydána z místa uložení do svého umístění uživatele, ale nemohl registrovat operaci výběru. Nekonzistentní data skladu jsou často, ale ne vždy, důvodem zablokování práce.

Na rozdíl od běžné funkce zrušení, ke které lze získat přístup pomocí tlačítka **zrušit** v záhlaví práce, nemusí funkce zrušení práce vyžadovat, aby byl poslední dokončený řádek práce řádkem **vyzvednout**. Jinými slovy, pro funkci zrušení práce lze spustit logiku zrušení i v případě, že se množství položky na řádku práce nachází v umístění uživatele.

> [!NOTE]
> V případě práce, která musí být zrušena z provozních důvodů, musí uživatelé skladu nadále používat pravidelné funkce zrušení na stránce práce.

Pomocí funkce Zrušit práci lze zrušit pouze práci typu **Prodej**, **Problém s převodem**, **Vyzvednutí surovin** nebo **Doplnění**. Logika zrušení nebude spuštěna pro zmrazenou práci výběru surovin nebo práci, kterou lze zrušit pomocí běžné funkce zrušení (Další informace naleznete v předchozí poznámce).

Chcete-li odblokovat práci, systém zruší všechny zbývající řádky práce a opraví data skladu přidružená k ID práce, kterou daný uživatel určil. Všechny běžné operace zpracování skladu, které zahrnují ovlivněné množství zboží, mohou být opět obnoveny.

Chcete-li po zrušení práce vložit ovlivněnou položku do určitého umístění, musí uživatel použít operaci pohybu zásob nebo úpravy množství v mobilním zařízení.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]