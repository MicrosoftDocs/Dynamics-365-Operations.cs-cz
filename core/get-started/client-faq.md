---
title: "Klient aplikace Dynamics 365 for Operations - často kladené dotazy"
description: "V tomto článku jsou odpovědi na časté otázky týkající se klienta Microsoft Dynamics 365 for Operations."
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

# <a name="dynamics-365-for-operations-client-faq"></a>Klient aplikace Dynamics 365 for Operations - často kladené dotazy

[!include[banner](../includes/banner.md)]


V tomto článku jsou odpovědi na časté otázky týkající se klienta Microsoft Dynamics 365 for Operations.

<a name="why-arent-symbols-loaded-when-i-use-dynamics-365-for-operations"></a>Proč se při používání Dynamics 365 for Operations nenačtou symboly?
-----------------------------------------------------------------

Nastavení zabezpečení ve vašem prohlížeči může bránit správnému načtení symbolů. K vyřešení problému proveďte následující kroky:

-   Pokud dochází k problému v prohlížeči Internet Explorer, klikněte na tlačítko **Nástroje**a potom klikněte na tlačítko **Možnosti Internetu**.  V dialogovém okně Možnosti Internetu na kartě **Ochrana osobních údajů** klikněte na **Vlastní úroveň**a ujistěte se, že je vybrána možnost **Stažení písma**.
-   V ostatních případech je třeba přidat server Dynamics 365 for Operations do seznamu důvěryhodných webů.

## <a name="i-miss-the-ribbon-from-dynamics-ax-2012-can-i-keep-action-pane-tabs-open-all-the-time"></a>Chybí mi pás karet z aplikace Dynamics AX 2012. Mohu nechat karty podokna akcí trvale otevřené?
Plánujeme přidání této funkce v blízké budoucnosti. Uživatelé pak budou moci ponechat karty podokna akcí trvale otevřené. V opačném případě se karty skryjí, když je uživatel nepoužívá, aby se uvolnilo místo na obrazovce pro stránku.

## <a name="why-do-i-sometimes-see-different-shortcut-menus-when-i-rightclick"></a>Proč se někdy při kliknutí pravým tlačítkem myši zobrazují jiné místní nabídky?
Když klepnete pravým tlačítkem myši do pole, které lze upravit (nebo pokud je vybraný text), se zobrazí v prohlížeči místní nabídka. Tato nabídka umožňuje přístup k příkazům **Vyjmout**, **Kopírovat** a **Vložit**. Z bezpečnostních důvodů nemůžeme tyto příkazy vložit do místní nabídky Dynamics 365 for Operations, protože prohlížeče nám neumožňují programátorsky přistupovat do schránky systému.

Když kliknete pravým tlačítkem myši na popisek pole nebo na hodnotu ovládacího prvku jen pro čtení, zobrazí se místní nabídka Dynamics 365 for Operations.

Aby byla práce s klávesnicí snazší, plánujeme v budoucnu implementovat funkci klávesových zkratek, která otevře místní nabídku aplikace Dynamics 365 for Operations.

## <a name="where-is-the-view-details-functionality-in-dynamics-365-for-operations"></a>Kde je funkce Zobrazit podrobnosti v aplikaci Dynamics 365 for Operations?
Volba **Zobrazit podrobnosti** je k dispozici v několika způsoby:

-   Má-li ovládací prvek schopnost **Zobrazit podrobnosti **a pokud má ovládací prvek hodnotu, tato hodnota je zobrazena jako hypertextový odkaz. Klepnutím na odkaz otevřete stránku, která obsahuje další podrobnosti.
-   Možnost **Zobrazit podrobnosti** je také v místní nabídce aplikace Dynamics 365 for Operations. Další informace o tom, kdy se místní nabídky aplikace Dynamics 365 for Operations zobrazí při kliknutí pravým tlačítkem myši, naleznete v předchozím oddílu.





