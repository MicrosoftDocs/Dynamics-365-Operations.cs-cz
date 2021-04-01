---
title: Nastavení pracovních postupů schvalování leasingu
description: V tématu je vysvětleno, jak nastavit pracovní postup schválení, který bude spuštěn při vytvoření nového leasingu.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 1eaa2f5cc191ec93c30f4f10a662a87e501a341d
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5249574"
---
# <a name="set-up-lease-approval-workflows"></a>Nastavení pracovních postupů schvalování leasingu

[!include [banner](../includes/banner.md)]

V tématu je vysvětleno, jak nastavit pracovní postup schválení, který bude spuštěn při vytvoření nového leasingu. Informace o tom, jak používat pracovní postup, najdete v části [Použití pracovních postupů schvalování leasingu](use-create-lease-wrkflw.md). 

1. Přejděte na **Leasing majetku \> Nastavení \> Pracovní postup leasingu**.
2. Na stránce **Pracovní postup leasingu** zvolte **Nový**.
3. V zobrazeném dialogovém okně v části **Typ pracovního postupu** vyberte odkaz **Pracovní postup pronájmu**.

    Aplikace je otevřena. Po spuštění se přihlaste k Azure Active Directory (Azure AD), abyste byli přesměrováni do aplikace pracovního postupu.

4. Přetáhněte prvek **Schválení pracovního postupu leasingu** do pracovního toku.
5. Připojte jeden uzel ze **Start** do **Schválení pracovního postupu leasingu**. Pak připojte **Schválení pracovního postupu leasingu** na **Konec**.
6. Dvakrát klikněte na **Schválení pracovního postupu leasingu**.
7. Vyberte **Vlastnosti** a poté v části **Základní nastavení** zadejte název pracovního postupu.

    Na této stránce můžete také nastavit další parametry pracovního postupu. Pokud jste zapnuli **Automatické akce**, systém automaticky provede konkrétní akci. Oznámení lze zasílat, pokud jsou uvedena na kartě **Oznámení**. Na kartě **Pokročilé nastavení** můžete určit konečného schvalovatele, nastavit časový limit a určit konkrétní akce, které je třeba dokončit.

8. Po dokončení nastavení parametrů pracovního postupu vyberte **Zavřít**.
9. Vyberte **Krok 1** a poté vyberte **Vlastnosti**.
10. V části **Základní nastavení** zadejte název kroku, vytvořte předmět pro schválení a zadejte pokyny ke schválení.
11. Na stránce **Úkol** vyberte typ přiřazení.
12. Chcete-li ke schválení přiřadit konkrétní uživatele, vyberte **Uživatel**, vyberte uživatele, kteří schvalují leasing, a poté vyberte **Zavřít**.
13. Vyberte **Uložit a zavřít** k vytvoření pracovního postupu. Po zobrazení výzvy vyberte **OK**.
14. Na stránce **Vytvořit pracovní postup** zvolte **Zavřít**.
14. Vyberte nový pracovní postup a pak vyberte **Verze**. Poté vyberte **Aktivovat** pro zajištění, aby byl pracovní postup aktivní.
15. Vyberte **Zavřít**. Zobrazí se nová aktivní verze.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]