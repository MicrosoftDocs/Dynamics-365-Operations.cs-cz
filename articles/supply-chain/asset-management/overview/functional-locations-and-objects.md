---
title: Funkční místa a majetek
description: Tento článek popisuje funkční místa a majetek v modulu Správa majetku. Správa majetku je rozšířený modul pro správu majetku a úloh údržby v aplikaci Dynamics 365 Supply Chain Management.
author: johanhoffmann
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 274e80136ee303af9d0fe5fd04095f575a345d19
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8875648"
---
# <a name="functional-locations-and-assets"></a>Funkční místa a majetek

[!include [banner](../../includes/banner.md)]

 

Tento článek popisuje funkční místa a majetek v modulu Správa majetku. Správa majetku je rozšířený modul pro správu majetku a úloh údržby v aplikaci Dynamics 365 Supply Chain Management.

## <a name="overview"></a>Přehled

Správa majetku je bezproblémově integrována s několika moduly v dalších aplikacích Finance and Operations. Následující ilustrace znázorňuje rozhraní s jinými moduly.

![Diagram znázorňující způsob, jakým jsou rozhraní správy majetku s jinými moduly.](media/01-overview-image.png)

Správa majetku umožňuje efektivně spravovat a provádět všechny úkoly související se správou a údržbou mnoha typů zařízení ve vaší firmě. Toto zařízení zahrnuje stroje, výrobní zařízení a vozidla. Správa majetku též podporuje řešení napříč četnými průmyslovými odvětvími.

Následující ilustrace znázorňuje přehled hlavních funkcí, které jsou pokryty správou majetku.

![Diagram znázorňující hlavní funkce ve správě majetku.](media/02-overview-image.png)

## <a name="functional-locations-and-assets"></a>Funkční místa a majetek

Funkční místa slouží ke správě majetku na místech. Tato správa zahrnuje sledování nákladů na majetek na funkčních místech. Funkční místa jsou strukturovaná hierarchicky a místa mohou mít dílčí místa. Struktura funkčních míst je statická. Jinými slovy, místa nemohou změnit místo. Majetek může být instalován na funkčních místech a podle potřeby může být později instalován na jiná funkční místa.

Náklady na majetek se vždy řídí místem majetku. Jinými slovy, pokud je majetek instalován na novém funkčním místě, majetek automaticky použije finanční dimenze, které souvisejí s novým funkčním místem. Proto jsou náklady na majetek vždy spojeny s funkčním místem, na kterém je majetek aktuálně nainstalován. Toto automatické zpracování finančních dimenzí zaručuje úplné sledování nákladů, když vaše společnost provádí kontrola a hlášení projektu na funkčních místech.

Způsob vytvoření hierarchie funkčních míst závisí na požadavcích vaší společnosti na údržbu interního vybavení nebo na údržbě vybavení zákazníka. Následující obrázek znázorňuje příklad funkčních míst, která jsou založena na zeměpisných lokalitách.

![Diagram znázorňující funkční místa na základě geografických umístění.](media/03-overview-image.png)

Následující obrázek znázorňuje příklad funkčních míst, která jsou založena na zákaznících.

![Diagram znázorňující funkční místa na základě zákazníků.](media/04-overview-image.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]