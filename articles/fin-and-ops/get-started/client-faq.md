---
title: "Nejčastější dotazy týkající se klienta aplikace Finance and Operations"
description: "V tomto článku jsou odpovědi na časté otázky týkající se klienta Microsoft Dynamics 365 for Finance and Operations."
author: jasongre
manager: AnnBe
ms.date: 10/23/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 12334
ms.assetid: a9a57f0e-a67c-46b1-83c9-5d6350fb3b86
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 3ee5334c87b2b0acae2afa6882feca63e3b9cc8e
ms.openlocfilehash: 74f85f7a1c390d1f21d0423a794ff16c7250d9fa
ms.contentlocale: cs-cz
ms.lasthandoff: 12/18/2018

---

# <a name="finance-and-operations-client-faq"></a>Nejčastější dotazy týkající se klienta aplikace Finance and Operations

[!include [banner](../includes/banner.md)]

V tomto článku jsou odpovědi na časté otázky týkající se klienta Microsoft Dynamics 365 for Finance and Operations.

## <a name="why-arent-symbols-loaded-when-i-use-finance-and-operations"></a>Proč se při používání Finance and Operations nenačtou symboly?

Nastavení zabezpečení ve vašem prohlížeči může bránit správnému načtení symbolů. K vyřešení problému proveďte následující kroky:

- Pokud dochází k problému v prohlížeči Internet Explorer, klikněte na tlačítko **Nástroje** a potom klikněte na tlačítko **Možnosti Internetu**. V dialogovém okně Možnosti Internetu na kartě **Ochrana osobních údajů** klikněte na **Vlastní úroveň** a ujistěte se, že je vybrána možnost **Stažení písma**.
- V ostatních případech je třeba přidat web Finance and Operations do seznamu důvěryhodných webů.

## <a name="i-miss-the-ribbon-from-dynamics-ax-2012-can-i-keep-action-pane-tabs-open-all-the-time"></a>Chybí mi pás karet z aplikace Dynamics AX 2012. Mohu nechat karty podokna akcí trvale otevřené?

Plánujeme přidání této funkce v blízké budoucnosti. Uživatelé pak budou moci ponechat karty podokna akcí trvale otevřené. V opačném případě se karty skryjí, když je uživatel nepoužívá, aby se uvolnilo místo na obrazovce pro stránku.

## <a name="why-do-i-sometimes-see-different-shortcut-menus-when-i-right-click"></a>Proč se někdy při kliknutí pravým tlačítkem myši zobrazují jiné místní nabídky?

Když klepnete pravým tlačítkem myši do pole, které lze upravit (nebo pokud je vybraný text), se zobrazí v prohlížeči místní nabídka. Tato nabídka umožňuje přístup k příkazům **Vyjmout**, **Kopírovat** a **Vložit**. Z bezpečnostních důvodů nemůžeme tyto příkazy vložit do místní nabídky Finance and Operations, protože prohlížeče nám neumožňují programátorsky přistupovat do schránky systému.

Když kliknete pravým tlačítkem myši na popisek pole nebo na hodnotu ovládacího prvku jen pro čtení, zobrazí se místní nabídka Finance and Operations.

Aby byla práce s klávesnicí snazší, plánujeme v budoucnu implementovat funkci klávesových zkratek, která otevře místní nabídku aplikace Finance and Operations.

## <a name="where-is-the-view-details-functionality-in-finance-and-operations"></a>Kde je funkce Zobrazit podrobnosti v aplikaci Finance and Operations?

Volba **Zobrazit podrobnosti** je k dispozici v několika způsoby:

- Má-li ovládací prvek schopnost **Zobrazit podrobnosti** a pokud má ovládací prvek hodnotu, tato hodnota je zobrazena jako hypertextový odkaz. Klepnutím na odkaz otevřete stránku, která obsahuje další podrobnosti.
- Možnost **Zobrazit podrobnosti** je také v místní nabídce aplikace Finance and Operations. Další informace o tom, kdy se místní nabídky aplikace Finance and Operations zobrazí při kliknutí pravým tlačítkem myši, naleznete v předchozím oddílu.

