---
title: "Dynamics 365 pro operace klienta, nejčastější dotazy"
description: "Tento článek poskytuje odpovědi na často kladené otázky týkající se služeb Microsoft Dynamics 365 pro operace klienta."
author: jasongre
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 12334
ms.assetid: a9a57f0e-a67c-46b1-83c9-5d6350fb3b86
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 4bb647cfd3f012efbffa93a81462c538a24ac850
ms.openlocfilehash: 2c99b2e1f7ddecb61be62832ca1a8d3ac1fd21a8
ms.lasthandoff: 03/31/2017


---

# <a name="dynamics-365-for-operations-client-faq"></a>Dynamics 365 pro operace klienta, nejčastější dotazy

[!include[banner](../includes/banner.md)]


Tento článek poskytuje odpovědi na často kladené otázky týkající se služeb Microsoft Dynamics 365 pro operace klienta.

<a name="why-arent-symbols-loaded-when-i-use-dynamics-365-for-operations"></a>Proč nejsou symboly načteny při použití Dynamics 365 pro operace?
-----------------------------------------------------------------

Nastavení zabezpečení ve vašem prohlížeči může bránit správnému načtení symbolů. K vyřešení problému proveďte následující kroky:

-   Pokud dojde k tomuto problému v aplikaci Internet Explorer, klepněte na tlačítko **nástroje**a potom klepněte na tlačítko **Možnosti Internetu**.  V dialogovém okně Možnosti Internetu na **osobních** karta, klepněte na **vlastní úroveň**a ujistěte se, **stažení písma** vybrána možnost.
-   Jinak je nutné přidat 365 Dynamics operace serveru do seznamu důvěryhodných webů.

## <a name="i-miss-the-ribbon-from-dynamics-ax-2012-can-i-keep-action-pane-tabs-open-all-the-time"></a>Zmeškání pásu karet z Dynamics AX 2012. Můžete ponechat v podokně akcí karty otevřete celou dobu?
Doporučujeme hodláte co nejdříve implementovat tuto funkci. Uživatelé pak budou moci zachovat karty na podokna akcí otevřít vždy. V opačném případě se karty skryjí, když je uživatel nepoužívá, aby se uvolnilo místo na obrazovce pro stránku.

## <a name="why-do-i-sometimes-see-different-shortcut-menus-when-i-rightclick"></a>Proč někdy vidět různé místní nabídky při I rightclick?
Když klepnete pravým tlačítkem myši do pole, které lze upravit (nebo pokud je vybraný text), se zobrazí v prohlížeči místní nabídka. Tato nabídka umožňuje přístup k příkazům **Vyjmout**, **Kopírovat** a **Vložit**. Jsme nelze vložit tyto příkazy do 365 Dynamics pro operace místní nabídky, protože z bezpečnostních důvodů není prohlížečů umožňuje nám programově přístup do schránky systému.

Pravým tlačítkem myši popisek pole nebo hodnoty ovládacího prvku jen pro čtení, zobrazí se 365 Dynamics pro operace místní nabídce.

Usnadnit přístup z klávesnice, plánujeme zavést klávesovou zkratku v budoucnu bude otevřen 365 Dynamics pro operace místní nabídce.

## <a name="where-is-the-view-details-functionality-in-dynamics-365-for-operations"></a>Funkci Zobrazit podrobnosti v 365 Dynamics pro operace kde je?
Volba **Zobrazit podrobnosti** je k dispozici v několika způsoby:

-   Má-li ovládací prvek schopnost **Zobrazit podrobnosti **a pokud má ovládací prvek hodnotu, tato hodnota je zobrazena jako hypertextový odkaz. Klepnutím na odkaz otevřete stránku, která obsahuje další podrobnosti.
-   **Zobrazit podrobnosti** je také možnost na Dynamics 365 pro operace místní nabídky. Další informace o tom, kdy Dynamics 365 pro operace místní nabídky se zobrazí po klepnutí pravým tlačítkem myši, naleznete v předchozí části.





