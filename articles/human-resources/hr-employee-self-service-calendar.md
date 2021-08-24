---
title: Vytvoření kalendáře týmu
description: Zobrazte a vytvořte kalendáře týmu v Dynamics 365 Human Resources.
author: andreabichsel
ms.date: 07/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EssWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ccbf12d4dcc75e22fc62c356653a91b9a8a8d1761ccefb18c93e65f343250830
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6744219"
---
# <a name="view-team-and-company-calendars"></a>Zobrazení kalendáře týmu a společnosti

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Můžete zobrazit kalendáře týmu a společnosti v Dynamics 365 Human Resources. Týmové kalendáře zobrazují pouze přímé podřízené definice v hierarchii řádků.

## <a name="view-your-team-calendar-as-an-employee"></a>Zobrazení týmového kalendáře jako zaměstnanec

- V pracovní prostoru **Zaměstnanecká samoobsluha** vyberte **Kalendář absence týmu** v **Souhrnu**.

## <a name="view-your-team-calendar-as-a-manager"></a>Zobrazení týmového kalendáře jako vedoucí

1. V pracovním prostoru **Samoobsluha zaměstnance** vyberte **Můj tým**.

2. Vyberte **Pracovní volno a absence** a poté vyberte **Zobrazit kalendář absence vedoucího**.

Manažeři také mohou přistupovat k týmovému kalendáři z **Nedokončených požadavků od mého týmu**, **Schváleného volna** a **Požadavků na volno**. 

## <a name="view-your-absence-manager-calendar-as-the-absence-manager"></a>Zobrazte svůj kalendář nepřítomnosti jako správce nepřítomnosti

> [!NOTE]
> Chcete-li zobrazit kalendář správce nepřítomnosti, musíte nejprve zapnout funkci **(Náhled) Správce nepřítomnosti pro správu dovolené** ve Správě funkcí. Další informace o zapnutí funkcí Preview naleznete v tématu [Správa funkcí](hr-admin-manage-features.md).

Uživatelé v roli Správce nepřítomnosti mohou ve svém kalendáři zobrazit žádosti o volno. Chcete-li získat přístup ke kalendáři dovolené, postupujte takto.

1. V pracovním prostoru **Samoobsluha zaměstnanců** vyberte **Správa pracovního volna** a pak **Kalendář správce nepřítomnosti**.

2. Do pole **Datum** zadejte požadované datum.

3. Podle potřeby aktualizujte možnosti zobrazení.

Kalendář správce nepřítomnosti zobrazuje všechny záznamy zaměstnanců, kteří se hlásí správci nepřítomnosti v hierarchii Dovolená.

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

> [!IMPORTANT]
> Můžete zapnout funkci **Zobrazení dovolené napříč společnostmi** v Správě funkcí. Poté musíte tuto funkci povolit na stránce **Sdílené parametry Human Resource** k zobrazení filtru právnické osoby v kalendářích. Další informace naleznete v tématu [Konfigurace parametrů pracovního volna a absence](hr-leave-and-absence-parameters.md).
> 
> Kalendář můžete filtrovat podle právnické osoby. Pokud chcete vidět všechny zaměstnance bez ohledu na právnickou osobu, zrušte zaškrtnutí políčka filtru a vyberte **Enter**. 

Informace o nastavení kalendáře naleznete v tématu [Konfigurace parametrů kalendáře](hr-leave-and-absence-parameters.md?configure-calendar-parameters).

[!INCLUDE[footer-include](../includes/footer-banner.md)]
