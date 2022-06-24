---
title: Zřízení Microsoft Teams z Dynamics 365 Commerce
description: Tento článek popisuje, jak zřídit Microsoft Teams pomocí organizačních dat z Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 3dc9d0f20ec251f0908dda0017adaaeac1b43856
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8868928"
---
# <a name="provision-microsoft-teams-from-dynamics-365-commerce"></a>Zřízení Microsoft Teams z Dynamics 365 Commerce

[!include [banner](includes/banner.md)]

Tento článek popisuje, jak zřídit Microsoft Teams pomocí organizačních dat z Dynamics 365 Commerce.

Dynamics 365 Commerce nabízí snadný způsob zřízení Teams, pokud jste tam dosud nenastavili týmy pro své maloobchodní prodejny. Využíváním výhod dobře definovaných informací z Commerce, které chcete použít v Teams, můžete svým zaměstnancům obchodu pomoci začít pracovat v Teams. Mezi tyto informace patří hierarchie organizace, názvy obchodů, informace o zaměstnancích a účty Azure Active Directory (Azure AD). 

Proces zřizování Teams má dva hlavní kroky:

1. V aplikaci Teams vytvořte tým pro každý maloobchod a přidejte pracovníky obchodu jako členy příslušného týmu. Pokud je zaměstnanec přidružen k více než jednomu maloobchodu, odráží tuto skutečnost členství v týmu. Bude vytvořen komunikační tým, který jako členy bude zahrnovat regionální manažery, aby pomohl publikovat úkoly z Teams.
1. Nahrajte svou organizační hierarchii z Commerce do Teams.

## <a name="provision-teams-in-commerce-headquarters"></a>Zřízení Teams v Commerce Headquarters

Před zřízením Microsoft Teams proveďte tyto úkoly:

- Potvrďte, že všichni regionální manažeři byli jmenováni správci komunikace.
- Potvrďte, že účet Azure každého manažera a pracovníka obchodu byl přidružen k záznamu pracovníka tohoto manažera nebo pracovníka v Commerce Headquarters.

Chcete-li zřídit Teams v Commerce Headquarters, postupujte takto.

1. Přejděte na **Retail a Commerce \> Nastavení kanálu \> Konfigurace integrace Microsoft Teams**.
1. V podokně akcí vyberte **Zřídit Teams**. Vytvoří se dávková úloha, která je pojmenována **Zřídit Teams**.
1. Přejděte na **Správa systému \> Dotazy \> Dávkové úlohy** a vyhledejte nejnovější úlohu s popisem **Zřízení Teams**. Počkejte, až se tato úloha dokončí.

> [!TIP]
> Pokud žádný z vašich regionálních manažerů, manažerů obchodů a pracovníků obchodů nebyl přidružen k licenci Teams, může se zobrazit následující chybová zpráva: „Nepodařilo se načíst použitelné kategorie SKU pro uživatele.“ Chcete-li problém vyřešit, vyberte **Synchronizovat týmy a členy** v podokně akcí.

<!-- ![Dynamics 365 Commerce - Teams integration configuration.](media/D365-Commerce-Microsoft-Teams-Configuration_with_disclaimer.png)-->

## <a name="validate-teams-provisioning-in-the-teams-admin-center"></a>Ověření zřízení Teams v centru pro správu Teams

Chcete-li ověřit zřízení Microsoft Teams v centru pro správu Microsoft Teams, postupujte podle těchto kroků.
    
1. Přejděte do [centra pro správu Teams](https://admin.teams.microsoft.com/) a přihlaste se jako správce vašeho klienta elektronického obchodu.
1. V levém navigačním podokně vyberte **Teams**, rozbalte ho a poté vyberte **Spravovat týmy**.
1. Potvrďte, že pro každý maloobchod Commerce byl vytvořen jeden tým.
1. Vyberte tým a potvrďte, že do něj byli přidáni pracovníci obchodu jako členové.
1. V levém navigačním podokně vyberte **Uživatelé** a potvrďte, že všichni zaměstnanci obchodu ve všech obchodech byli přidáni jako uživatelé.

Následující obrázek ukazuje příklad stránky **Spravovat týmy** v centru pro správu Teams.

![Příklad stránky Spravovat týmy v centru pro správu Teams.](media/Teams-FLW-Admin-Teams.png)

## <a name="upload-a-commerce-organizational-hierarchy-to-teams"></a>Nahrajte organizační hierarchii Commerce do Teams.
    
Lze použít hierarchii organizace Commerce v Microsoft Teams a publikovat úkoly do všech nebo vybraných obchodů, které používají stejnou hierarchickou strukturu.

Pokud chcete odeslat organizační hierarchii Commerce do Teams, postupujte následovně.
    
1. V Commerce Headquarters přejděte na možnost **Retail a Commerce \> Nastavení kanáu \> Konfigurace integrace Microsoft Teams**.
1. Vyberte **Stáhnout cílovou hierarchii** a potom vyberte **Maloobchody podle regionu** ke stažení souboru hodnot oddělených čárkami (CSV) hierarchie organizace.
1. Nainstalujte modul Microsoft Teams PowerShell podle pokynů v části [Instalace Microsoft Teams PowerShell](/microsoftteams/teams-powershell-install).
1. Po zobrazení výzvy v okně Teams PowerShell se přihlaste pomocí účtu správce pro svého klienta Azure AD.
1. Postupujte podle pokynů v části [Nastavení cílové hierarchie týmů](/microsoftteams/set-up-your-team-hierarchy) a nahrajte soubor CSV pro cílovou hierarchii.

## <a name="verify-that-the-organizational-hierarchy-was-uploaded-to-teams"></a>Ověření, že byla do Teams nahrána hierarchie organizace

Chcete-li ověřit, že byla do Microsoft Teams nahrána hierarchie organizace, postupujte takto.

1. Přihlaste se k Teams jako manažer komunikace.
1. V levém navigačním podokně vyberte **Úkoly Planner**.
1. Na kartě **Publikované seznamy** vytvořte nový seznam, který má fiktivní úkol.
1. Zvolte **Publikovat**. Hierarchie organizace by se měla objevit v dialogovém okně **Vyberte, komu publikovat**, jak je znázorněno v příkladu na následujícím obrázku.

![Příklad hierarchie organizace v dialogovém okně Vyberte, komu publikovat.](media/Microsoft-teams-verify-org-hierarchy.png)

## <a name="additional-resources"></a>Další prostředky

[Přehled integrace Dynamics 365 Commerce a Microsoft Teams](commerce-teams-integration.md)

[Povolení integrace Dynamics 365 Commerce a Microsoft Teams](enable-teams-integration.md)

[Synchronizace správy úkolů mezi Microsoft Teams a Dynamics 365 Commerce POS](synchronize-tasks-teams-pos.md)

[Správa uživatelských rolí v Microsoft Teams](manage-user-roles-teams.md)

[Mapování obchodů a týmů, pokud v Microsoft Teams již existují přednastavené týmy](map-stores-existing-teams.md)

[Nejčastější dotazy k integraci Dynamics 365 Commerce a Microsoft Teams](teams-integration-faq.md)