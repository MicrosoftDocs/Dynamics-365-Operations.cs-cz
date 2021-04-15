---
title: Vytvoření kalendáře týmu
description: Zobrazte a vytvořte kalendáře týmu v Dynamics 365 Human Resources.
author: andreabichsel
ms.date: 11/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EssWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 07c7f1303238fe61d70be26ec5a198f1ac489090
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5790757"
---
# <a name="view-team-and-company-calendars"></a>Zobrazení kalendáře týmu a společnosti

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Můžete zobrazit kalendáře týmu a společnosti v Dynamics 365 Human Resources. Týmové kalendáře zobrazují pouze přímé podřízené definice v hierarchii řádků.

## <a name="view-your-team-calendar-as-an-employee"></a>Zobrazení týmového kalendáře jako zaměstnanec

1. V pracovní prostoru **Zaměstnanecká samoobsluha** vyberte **Kalendář absence týmu** v **Souhrnu**.

## <a name="view-your-team-calendar-as-a-manager"></a>Zobrazení týmového kalendáře jako vedoucí

1. V pracovním prostoru **Samoobsluha zaměstnance** vyberte **Můj tým**.

2. Vyberte **Pracovní volno a absence** a poté vyberte **Zobrazit kalendář absence vedoucího**.

Manažeři také mohou přistupovat k týmovému kalendáři z **Nedokončených požadavků od mého týmu**, **Schváleného volna** a **Požadavků na volno**. 

## <a name="view-a-company-calendar"></a>Zobrazit kalendář společnosti

Uživatelé, kteří jsou v rolích lidských zdrojů, mohou zobrazit kalendáře společnosti. V kalendářích společnosti jsou zobrazeni všichni zaměstnanci. Ve výchozím nastavení zobrazuje kalendář dnešní datum plus 28 dní, ale rozsah dat lze změnit. Můžete také filtrovat kalendář podle **názvu**, **čísla pracovníka** a **typu** pracovního volna.

1. V pracovním prostoru **Pracovní volno a absence** vyberte kartu **Odkazy**.

2. Vyberte **Kalendář pracovního volna a absence**.

Role lidských zdrojů mají také přístup k kalendáři společnosti z **Žádosti o pracovní volno a absenci**, **Schválené volno** a **Žádosti o volno**. 

Kalendáře nyní obsahují další filtry a možnosti. Všechny kalendáře obsahují možnosti zobrazení pro:

- Schválené požadavky
- Žádosti čekající na vyřízení
- Zaměstnance s žádostmi o pracovní volno
- Zaměstnance bez žádostí o pracovní volno
- Narozeniny zaměstnanců
- Žádosti o volno 
- Žádosti o pracovní volno

Konfigurace kalendáře v parametrech Pracovní volno a absence určuje dostupné možnosti zobrazení.

Můžete také filtrovat kalendáře podle manažera nebo oddělení. Přiřazení primární pozice určuje zaměstnance zobrazené při nastavení těchto filtrů. 

>[!IMPORTANT]
>Zobrazení pracovního volna a absencí napříč společnostmi je aktuálně ve verzi Preview. Budete to muset povolit ve svém prostředí **Sandbox**. Další informace o povolení funkcí verze Preview naleznete v tématu [Správa funkcí](hr-admin-manage-features.md).<br><br>
>Poté musíte tuto funkci povolit v části **Sdílené parametry Human Resource** k zobrazení filtru právnické osoby v kalendářích. Další informace naleznete v tématu [Konfigurace parametrů pracovního volna a absence](hr-leave-and-absence-parameters.md).<br><br>
>Kalendář můžete filtrovat podle právnické osoby. Pokud chcete vidět všechny zaměstnance bez ohledu na právnickou osobu, zrušte zaškrtnutí políčka filtru a stiskněte Enter. 

Informace o nastavení kalendáře naleznete v tématu [Konfigurace parametrů kalendáře](hr-leave-and-absence-parameters.md?configure-calendar-parameters).



[!INCLUDE[footer-include](../includes/footer-banner.md)]