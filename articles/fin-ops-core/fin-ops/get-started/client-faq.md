---
title: Často kladené dotazy ke klientovi
description: V tomto článku jsou odpovědi na časté otázky týkající se klienta financí a provozu.
author: jasongre
ms.date: 09/11/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.custom: 12334
ms.assetid: a9a57f0e-a67c-46b1-83c9-5d6350fb3b86
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ca763f388bfc59951febf93f314d3df7e12c50cf
ms.sourcegitcommit: 873d66c03a51ecb7082e269f30f5f980ccd9307f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/06/2022
ms.locfileid: "9124421"
---
# <a name="client-faq"></a>Často kladené dotazy ke klientovi

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

V tomto článku jsou odpovědi na časté otázky týkající se klienta financí a provozu.

## <a name="why-arent-symbols-loaded"></a>Proč nejsou načteny symboly?

Nastavení zabezpečení ve vašem prohlížeči může bránit správnému načtení symbolů. K vyřešení problému proveďte následující kroky:

- Pokud dochází k problému v prohlížeči Internet Explorer, klikněte na **Nástroje** a potom klikněte na tlačítko **Možnosti Internetu**. V dialogovém okně Možnosti Internetu na kartě **Ochrana osobních údajů** klikněte na **Vlastní úroveň** a ujistěte se, že je vybrána možnost **Stažení písma**.
- V ostatních případech je třeba přidat web aplikace do seznamu důvěryhodných webů.

## <a name="i-miss-the-ribbon-from-dynamics-ax-2012-can-i-keep-action-pane-tabs-open-all-the-time"></a>Chybí mi pás karet z aplikace Dynamics AX 2012. Mohu nechat karty podokna akcí trvale otevřené?

Plánujeme přidání této funkce v blízké budoucnosti. Uživatelé pak budou moci ponechat karty podokna akcí trvale otevřené. V opačném případě se karty skryjí, když je uživatel nepoužívá, aby se uvolnilo místo na obrazovce pro stránku.

## <a name="why-do-i-sometimes-see-different-shortcut-menus-when-i-right-click"></a>Proč se někdy při kliknutí pravým tlačítkem myši zobrazují jiné místní nabídky?

Když klepnete pravým tlačítkem myši do pole, které lze upravit (nebo pokud je vybraný text), se zobrazí v prohlížeči místní nabídka. Tato nabídka umožňuje přístup k příkazům **Vyjmout**, **Kopírovat** a **Vložit**. Z bezpečnostních důvodů nemůžeme tyto příkazy vložit na místní nabídky, protože prohlížeče neumožňují programu přistupovat do schránky systému.

Když kliknete pravým tlačítkem myši na popisek pole nebo na hodnotu ovládacího prvku jen pro čtení, zobrazí se místní nabídka.

Aby byla práce s klávesnicí snazší, plánujeme v budoucnu implementovat funkci klávesových zkratek, která otevře místní nabídku.

## <a name="where-is-the-view-details-functionality"></a>Kde je funkce Zobrazit podrobnosti?

Volba **Zobrazit podrobnosti** je k dispozici v několika způsoby:

- Má-li ovládací prvek schopnost **Zobrazit podrobnosti** a pokud má ovládací prvek hodnotu, tato hodnota je zobrazena jako hypertextový odkaz. Klepnutím na odkaz otevřete stránku, která obsahuje další podrobnosti.
- Možnost **Zobrazit podrobnosti** je také v místní nabídce. Další informace o tom, kdy se místní nabídky zobrazí při klepnutí pravým tlačítkem myši, naleznete v předchozím oddílu.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
