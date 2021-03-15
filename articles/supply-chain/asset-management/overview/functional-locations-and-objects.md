---
title: Funkční místa a majetek
description: Toto téma popisuje funkční místa a majetek v modulu Správa majetku. Správa majetku je rozšířený modul pro správu majetku a úloh údržby v aplikaci Dynamics 365 Supply Chain Management.
author: josaw1
manager: tfehr
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2f93a68f19b0b952eb2964b404bb957865c625cd
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/16/2021
ms.locfileid: "5018039"
---
# <a name="functional-locations-and-assets"></a>Funkční místa a majetek

[!include [banner](../../includes/banner.md)]

 

Toto téma popisuje funkční místa a majetek v modulu Správa majetku. Správa majetku je rozšířený modul pro správu majetku a úloh údržby v aplikaci Dynamics 365 Supply Chain Management.

## <a name="overview"></a>Přehled

Správa majetku je bezproblémově integrována s několika moduly v dalších aplikacích Finance and Operations. Následující ilustrace znázorňuje rozhraní s jinými moduly.

![Diagram znázorňující způsob, jakým jsou rozhraní správy majetku s jinými moduly](media/01-overview-image.png)

Správa majetku umožňuje efektivně spravovat a provádět všechny úkoly související se správou a údržbou mnoha typů zařízení ve vaší firmě. Toto zařízení zahrnuje stroje, výrobní zařízení a vozidla. Správa majetku též podporuje řešení napříč četnými průmyslovými odvětvími.

Následující ilustrace znázorňuje přehled hlavních funkcí, které jsou pokryty správou majetku.

![Diagram znázorňující hlavní funkce ve správě majetku](media/02-overview-image.png)

## <a name="functional-locations-and-assets"></a>Funkční místa a majetek

Funkční místa slouží ke správě majetku na místech. Tato správa zahrnuje sledování nákladů na majetek na funkčních místech. Funkční místa jsou strukturovaná hierarchicky a místa mohou mít dílčí místa. Struktura funkčních míst je statická. Jinými slovy, místa nemohou změnit místo. Majetek může být instalován na funkčních místech a podle potřeby může být později instalován na jiná funkční místa.

Náklady na majetek se vždy řídí místem majetku. Jinými slovy, pokud je majetek instalován na novém funkčním místě, majetek automaticky použije finanční dimenze, které souvisejí s novým funkčním místem. Proto jsou náklady na majetek vždy spojeny s funkčním místem, na kterém je majetek aktuálně nainstalován. Toto automatické zpracování finančních dimenzí zaručuje úplné sledování nákladů, když vaše společnost provádí kontrola a hlášení projektu na funkčních místech.

Způsob vytvoření hierarchie funkčních míst závisí na požadavcích vaší společnosti na údržbu interního vybavení nebo na údržbě vybavení zákazníka. Následující obrázek znázorňuje příklad funkčních míst, která jsou založena na zeměpisných lokalitách.

![Diagram znázorňující funkční místa na základě geografických umístění](media/03-overview-image.png)

Následující obrázek znázorňuje příklad funkčních míst, která jsou založena na zákaznících.

![Diagram znázorňující funkční místa na základě zákazníků](media/04-overview-image.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]