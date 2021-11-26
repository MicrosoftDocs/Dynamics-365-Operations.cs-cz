---
title: Vytvoření kalendáře pracovní doby
description: Definujte kalendář pracovní doby, svátků a časy, kdy nepracujete, v Dynamics 365 Human Resources.
author: twheeloc
ms.date: 10/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 09449b832c403b0f711c3827ad20fc5aa618fbc4
ms.sourcegitcommit: 1cc56643160bd3ad4e344d8926cd298012f3e024
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/02/2021
ms.locfileid: "7731485"
---
# <a name="create-a-working-time-calendar"></a>Vytvoření kalendáře pracovní doby

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Kalendář pracovní doby v aplikaci Dynamics 365 Human Resources zobrazuje dny a hodiny, které zaměstnanci pracují ve vaší organizaci. Když zaměstnanec odešle požadavek na volno, nemusí se starat o svátky a uzávěrky.

Chcete-li zefektivnit zpracování požadavků na vyřízení, konfigurujte pro vaši organizaci tyto položky:

- Kalendář pracovní doby
- Svátky a uzavírky
- Nepracovní doba

Při nastavování kalendáře pracovní doby můžete přidat poslední dvě položky. Lze je také konfigurovat nebo aktualizovat samostatně.

## <a name="set-up-a-working-time-calendar"></a>Nastavení kalendáře pracovní doby

Nastavte nejméně jeden kalendář pracovní doby, který zobrazuje dny a hodiny operace. Pokud používáte umístění ve více zemích a oblastech, můžete pro každou oblast nastavit kalendář pracovní doby.

1. Na stránce **Správa organizace** klikněte na **Kalendáře**.

2. Zvolte **Nová** a zadejte název a popis nové skupiny pro kalendář.

3. V části **Možnosti generování** vyberte pracovní dny pro organizaci a zadejte pracovní dobu. 
   - Chcete-li přidat svátek nebo uzavírku, vyberte tlačítko **Přidat** vedle **Svátky a uzávěrky**.
   - Chcete-li přidat nepracovní čas, například obědy nebo přestávky, vyberte **Přidat** v části **MIMOPRACOVNí DOBA** a zadejte název a časový rozsah.

4. Na kartě **Dny** zvolte **Generovat** a vygenerujte dny ve svém kalendáři. Zadejte rozsah dat pro svůj kalendář a poté vyberte možnost **Generovat dny**.

5. Chcete-li přidat pracovní plány, v části **Pracovní plán** vyberte **Přidat** a zadejte časy pro jednotlivé pracovní plány.

## <a name="configure-holidays-and-closures"></a>Konfigurace svátků a uzavírek

Svátky a uzávěrky lze přidávat a měnit odděleně od kalendáře pracovní doby.

1. Na stránce **Správa organizace** klikněte na **Svátky a uzavírky**.

2. Zvolte **Nová** a zadejte název a datum dovolené nebo uzavírky.

## <a name="configure-non-work-time"></a>Konfigurace mimopracovní doby

Svátky a uzavírky lze přidávat nebo lze měnit mimopracovní dobu odděleně od kalendáře pracovní doby.

1. Na stránce **Správa organizace** klikněte na **NEPRACOVNÍ DOBA**.

2. Vyberte **Nový** a zadejte název a časový rozsah mimopracovní doby.

Pokud jste aktivovali funkci náhledu oprav pracovního volna a svátků, Aplikace Human Resources použije data svátků a dat uzavírky k určení počtu dní, které se mají upravit pro zaměstnance zapsané v kalendáři.

## <a name="see-also"></a>Viz také

- [Přehled pracovního volna a absencí](hr-leave-and-absence-overview.md)
- [Konfigurace typů pracovního volna a absence](hr-leave-and-absence-types.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
