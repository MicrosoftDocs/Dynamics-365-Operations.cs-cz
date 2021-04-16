---
title: Omezení úpravy osobních údajů
description: U zaměstnanců můžete omezit jejich upravování kontaktních údajů v aplikaci Dynamics 365 Human Resources.
author: andreabichsel
ms.date: 03/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: EssWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-03-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 727e0d4dbc5b330045bc9f91abab4d43b09e4382
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5794798"
---
# <a name="restrict-editing-of-personal-information"></a>Omezení úpravy osobních údajů

[!include [applies to](../includes/applies-to-hr.md)]
[!include [preview feature](./includes/preview-feature.md)]

Toto téma popisuje, jak omezit zaměstnance v úpravách kontaktních údajů v aplikaci Dynamics 365 Human Resources. Možná budete chtít zabránit zaměstnancům v úpravách určitých kontaktních údajů, například jejich sídla firmy nebo e-mailové adresy.

> [!NOTE]
> Chcete-li použít tuto funkci, musíte nejprve povolit funkci **(Preview) Omezit zaměstnance v přidávání nebo úpravách adresy a kontaktních údajů pro vybrané účely** ve Správě funkcí. Další informace o povolení funkcí Preview naleznete v tématu [Správa funkcí](hr-admin-manage-features.md).<br><br>![Povolit funkci Preview](./media/hr-employee-self-service-restrict-enable.png)

## <a name="choose-the-information-an-employee-can-add-or-edit"></a>Vyberte informace, které zaměstnanec může přidat nebo upravit

1. V Human Resources vyberte možnost **Správa zaměstnanců**, vyberte **Odkazy** a poté vyberte **Parametry lidských zdrojů**.

   ![Přechod na parametry lidských zdrojů](./media/hr-employee-self-service-human-resources-parameters.png)

2. Na stránce **Parametry lidských zdrojů** vyberte kartu **Samoobsluha pro zaměstnance**.

   ![Výběr Samoobsluhy pro zaměstnance](./media/hr-employee-self-service-tab.png)

3. Na kartě **Samoobsluha pro zaměstnance** zrušte zaškrtnutí všech informací v části **Adresa a kontaktní informace**, kterou zaměstnanci nemají přidávat nebo upravovat. V tomto příkladu jsme zrušili zaškrtnutí **Obchodních** kontaktních informací.

   ![Omezení úprav obchodních kontaktních údajů](./media/hr-employee-self-service-restrict-business.png)

4. Zvolte **Uložit**.

   ![Uložit změny](./media/hr-employee-self-service-restrict-save.png)

## <a name="employee-experience"></a>Zkušenosti zaměstnanců

Poté, co jste omezili zaměstnance v přidávání nebo úpravách kontaktních údajů, mohou tyto informace zobrazit, ale nemohou je změnit.

V tomto příkladu, kde jsou zaměstnanci omezeni v úpravách **Obchodních** kontaktních údajů, mohou i nadále vidět informace v Samoobsluze pro zaměstnance:

![Zobrazení obchodních kontaktních údajů](./media/hr-employee-self-service-restrict-view.png)

Když však vyberou obchodní kontaktní údaje, podokno **Upravit adresu** se zobrazí jen ke čtení a nemohou v něm změnit žádné z polí.

![Podrobnosti o obchodním kontaktu se zobrazují jen ke čtení](./media/hr-employee-self-service-restrict-read-only.png)

Kromě toho, pokud vyberou možnost **Přidat** za účelem přidání nové adresy, nemohou vybrat v rozevíracím poli **Účel** hodnotu **Obchodní**.

![Zaměstnanec nemůže přidat obchodní adresu](./media/hr-employee-self-service-restrict-add.png)

To samé zaměstnanci zažijí při výběru části **Kontaktní údaje** na stránce **Osobní informace** a pokusu o přidání nové adresy. Rozevírací seznam **Účel** zobrazuje pouze ty typy informací, které mohou přidat. 

![Zaměstnanec nemůže vybrat položku Obchodní v rozevírací nabídce Účel](./media/hr-employee-self-service-restrict-purpose.png)

**Kontaktní údaje** nyní ukazují v mřížce údaj **Účel**.

![Účel se zobrazí v mřížce podrobností kontaktu](./media/hr-employee-self-service-restrict-purpose-grid.png)

## <a name="see-also"></a>Viz také

[Přehled samoobsluhy pro zaměstnance a manažera](hr-employee-manager-self-service-overview.md)<br>
[Konfigurace parametrů Human Resources](hr-setup-parameters.md)<br>
[Upravit osobní informace](hr-employee-manager-self-service-edit-personal-information.md)