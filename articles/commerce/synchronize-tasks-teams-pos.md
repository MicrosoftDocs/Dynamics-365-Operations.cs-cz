---
title: Synchronizace správy úkolů mezi Microsoft Teams a Dynamics 365 Commerce POS
description: Tento článek popisuje, jak synchronizovat správu úloh mezi pokladním místem (POS) Microsoft Teams a Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 11/04/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: f339ae031f11ad850dab47f84bc9823cf6776e74
ms.sourcegitcommit: 9e2e54ff7d15aa51e58309da3eb52366328e199d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/04/2022
ms.locfileid: "9746090"
---
# <a name="synchronize-task-management-between-microsoft-teams-and-dynamics-365-commerce-pos"></a>Synchronizace správy úkolů mezi Microsoft Teams a Dynamics 365 Commerce POS

[!include [banner](includes/banner.md)]

Tento článek popisuje, jak synchronizovat správu úloh mezi pokladním místem (POS) Microsoft Teams a Dynamics 365 Commerce.

Jedním z hlavních účelů integrace Teams je umožnit synchronizaci správy úkolů mezi aplikací POS a Teams. Tímto způsobem mohou zaměstnanci úložiště používat ke správě úkolů buď aplikaci POS nebo Teams, aniž by mezi nimi přepínali.

Protože Planner se používá jako úložiště pro úkoly v Teams, musí existovat propojení mezi Teams a Dynamics 365 Commerce. Tento odkaz je vytvořen pomocí ID konkrétního plánu pro daný tým obchodu.

Následující postupy ukazují, jak nastavit synchronizaci správy úloh mezi aplikacemi POS a Teams.

## <a name="link-pos-and-teams-for-task-management"></a>Propojení aplikací POS a Teams pro správu úkolů

Abyste propojili aplikace POS a Microsoft Teams za účelem správy úkolů v centrále Commerce, postupujte takto.

> [!NOTE]
> Než se pokusíte integrovat správu úloh s Teams, ujistěte se, že jste povolili [integraci Dynamics 365 Commerce a Microsoft Teams](enable-teams-integration.md). 

1. Jděte na **Retail a Commerce \> Správa úkolů \> Integrace úkolů s Microsoft Teams**.
1. V podokně akcí vyberte **Upravit**.
1. Nastavte možnost **Povolit integraci správy úkolů** na **Ano**.
1. V podokně akcí vyberte **Uložit**.
1. V podokně akcí vyberte **Nastavit správu úkolů**. Mělo by se zobrazit oznámení s informací, že se vytváří dávková úloha s názvem **Zřízení Teams**.
1. Přejděte na **Správa systému \> Dotazy \> Dávkové úlohy** a vyhledejte nejnovější úlohu s popisem **Zřízení Teams**. Počkejte, až se tato úloha dokončí.
1. Spusťte **Úloha CDX 1070**, abyste publikovali ID plánu a uložili odkazy na Retail Server.

## <a name="publish-a-test-task-list-in-teams"></a>Publikování seznamu testovacích úkolů v Teams

Následující postup předpokládá, že týmy vašeho obchodu používají integraci správy úkolů Microsoft Teams s Commerce poprvé.

Chcete-li v Teams publikovat seznam testovacích úkolů, postupujte takto.

1. Přihlaste se k Teams jako manažer komunikace. Manažeři komunikace jsou obvykle uživatelé, kteří mají v Commerce roli **Regionální manažer**.
1. V levém navigačním podokně vyberte **Úkoly Planner**.
1. Na kartě **Publikované seznamy** vyberte **Nový seznam** v levém dolním rohu a pojmenujte nový seznam jako **Seznam testovacích úkolů**.
1. Vyberte **Vytvořit**. Nový seznam se zobrazí v sekci **Koncepty**.
1. V sekci **Název úkolu** pojmenujte první úkol jako **Integrace testovacích týmů**. Poté stiskněte **Vstup**.
1. V seznamu **Koncepty** vyberte seznam úkolů. Poté vyberte  **Publikovat**  v pravém horním rohu.
1. V dialogovém okně **Vyberte, komu publikovat** vyberte týmy, které by měly obdržet seznam testovacích úkolů.
1. Vyberte **Další** a zkontrolujte svůj publikační plán. Pokud musíte provést změny, vyberte  **Zpět**. 
1. Vyberte **Potvrdit a pokračovat** a potom vyberte **Publikovat**.
1. Po dokončení publikování se v horní části karty **Publikované seznamy** zobrazí zpráva se sdělením, zda byl váš seznam úkolů úspěšně doručen.

Další informace viz [Publikování seznamů úkolů pro vytváření a sledování práce ve vaší organizaci](https://support.microsoft.com/office/publish-task-lists-to-create-and-track-work-in-your-organization-095409b3-f5af-40aa-9f9e-339b54e705df).

> [!NOTE]
> Po úspěšném publikování seznamu úkolů v Teams se úkoly zobrazí v POS. Manažeři POS a pokladní pak musí zapnout přihlášení Azure AD do POS. Další informace naleznete v článku [Povolit ověření Azure Active Directory pro přihlášení do POS](aad-pos-logon.md). 

## <a name="additional-resources"></a>Další prostředky

[Přehled integrace Dynamics 365 Commerce a Microsoft Teams](commerce-teams-integration.md)

[Povolení integrace Dynamics 365 Commerce a Microsoft Teams](enable-teams-integration.md)

[Zřízení Microsoft Teams z Dynamics 365 Commerce](provision-teams-from-commerce.md)

[Správa uživatelských rolí v Microsoft Teams](manage-user-roles-teams.md)

[Mapování obchodů a týmů, pokud v Microsoft Teams již existují přednastavené týmy](map-stores-existing-teams.md)

[Nejčastější dotazy k integraci Dynamics 365 Commerce a Microsoft Teams](teams-integration-faq.md)
