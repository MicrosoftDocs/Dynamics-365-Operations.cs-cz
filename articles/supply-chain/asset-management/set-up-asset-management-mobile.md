---
title: Nastavení mobilního pracovního prostoru správy majetku
description: Toto téma popisuje, jak nastavit mobilní aplikace Microsoft Dynamics 365 Supply Chain Management a Finance and Operations (Dynamics 365) pro spuštění mobilního pracovního prostoru Asset management, který mohou pracovníci použít k provádění úkolů správy majetku.
author: johanhoffmann
manager: tfehr
ms.date: 01/15/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-12-22
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 54da27a022dcc800438b96224370228aa8eed261
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5226140"
---
# <a name="set-up-the-asset-management-mobile-workspace"></a>Nastavení mobilního pracovního prostoru správy majetku

[!include [banner](../includes/banner.md)]

Toto téma popisuje, jak nastavit mobilní aplikace Microsoft Dynamics 365 Supply Chain Management a Finance and Operations (Dynamics 365) ke správě mobilního pracovního prostoru **Správa majetku**, který mohou pracovníci používat k provádění úkolů správy majetku.

## <a name="set-up-maintenance-worker-users-in-supply-chain-management"></a>Nastavení uživatelů pracovníků údržby v Supply Chain Management

Pro každého uživatele, který vyžaduje přístup do mobilního pracovního prostoru **Správa majetku**, postupujte následovně.

1. V části Supply Chain Management přejděte na **Lidské zdroje \> Pracovníci** a ujistěte se, že existuje pracovní záznam pro uživatele, kterého chcete nastavit. Podle potřeby vytvořte nový záznam pracovníka.
1. Jděte na **Správa majetku \> Nastavení \> Pracovníci \> Pracovníci** a ujistěte se, že je záznam pracovníka, který jste identifikovali (nebo vytvořili) v předchozím kroku, je namapován na záznam pracovníka údržby. Podle potřeby vytvořte nový záznam pracovníka údržby a nastavte pole **Pracovník** na záznam pracovníka z předchozího kroku.
1. Jděte na **Správa majetku \> Nastavení \> Pracovníci \> Skupina pracovníků údržby** a ujistěte se, že záznam pracovníka údržby, který jste identifikovali (nebo vytvořili) v předchozím kroku, patří do skupiny pracovníků údržby.
1. Přejděte do nabídky **Správa systému \> Uživatelé**.
1. Vyberte relevantního uživatele v mřížce.
1. Na kartě s náhledem **Detaily uživatele** nastavte pole **Osoba** na pracovní účet, který chcete přidružit k aktuálnímu uživatelskému účtu. Tento pracovní účet by měl být pracovním záznamem, který jste identifikovali (nebo vytvořili) v kroku 1 a namapovali na záznam pracovníka údržby v kroku 2.

> [!NOTE]
> Na funkce systému Windows se vztahují uživatelská oprávnění a role zabezpečení mobilního pracovního prostoru **Správa majetku**, stejně jako se vztahují na funkce uživatelského rozhraní Supply Chain Management. Proto musí každý uživatel, kterého jste nastavili pro přístup do mobilního pracovního prostoru **Správa majetku**, mít role zabezpečení, které jsou vyžadovány k provádění podobných operací přímo ve správě dodavatelského řetězce.

## <a name="publish-the-asset-management-mobile-workspace"></a>Publikování mobilního pracovního prostoru správy majetku

Pro zpřístupnění funkcí správy aktiv v mobilní aplikaci Finance and Operations (Dynamics 365) musíte publikovat mobilní pracovní prostor **Správa majetku**.

1. V části Supply Chain Management vyberte tlačítko **Nastavení** (symbol ozubeného kola v pravém horním rohu) a poté v nabídce vyberte **Mobilní aplikace**.
1. V dialogovém okně **Spravovat mobilní aplikaci** najděte dlaždici **Správa majetku**. Pokud obsahuje text „V metadatech - nepublikováno,“ pracovní prostor ještě nebyl publikován. Pokud obsahuje text „V metadatech - publikováno,“ pracovní prostor již byl publikován a zbytek tohoto postupu můžete přeskočit.

    ![Dialogové okno Správa mobilní aplikace](media/mobile-workspaces.png "Dialogové okno Správa mobilní aplikace")

1. Vyberte dlaždici **Správa majetku** a poté vyberte **Publikovat** na panelu nástrojů. Po několika sekundách byste měli obdržet oznámení, které uvádí, že pracovní prostor byl úspěšně publikován. Text na dlaždici by se měl navíc změnit na „V metadatech - publikováno“.

## <a name="install-and-set-up-the-finance-and-operations-dynamics-365-mobile-app"></a>Nainstalujte a nastavte mobilní aplikaci Finance and Operations (Dynamics 365)

1. Chcete-li nainstalovat **Microsoft Finance and Operations (Dynamics 365)**, přejděte do jednoho z následujících obchodů s aplikacemi na vašem mobilním zařízení:

    - [Pro zařízení Google Android](https://go.microsoft.com/fwlink/?linkid=850662)
    - [Pro zařízení Apple iOS](https://go.microsoft.com/fwlink/?linkid=850663)

1. Otevřete aplikaci Finance and Operations (Dynamics 365). Měla by se zobrazit přihlašovací stránka. Do pole **Přihlásit se** zadejte adresu URL pro správu dodavatelského řetězce nebo vyberte poslední adresu URL v seznamu **Nedávná prostředí** a potom klepněte na **Připojit**.

    ![Přihlašovací stránka](media/mobile-app-sign-in.png "Přihlašovací stránka")

1. Pokud se zobrazí výzva k potvrzení připojení, zaškrtněte políčko **Rozumím** a potom klepněte na **Připojit**.
1. Na stránce **Vyberte účet** použijte svůj účet Microsoft k přihlášení do mobilní aplikace.

    Zobrazí se stránka **Pracovní prostory**. Uvádí seznam všech mobilních pracovních prostorů, které byly publikovány vaší instancí Supply Chain Management.

    ![Seznam pracovních prostorů](media/mobile-app-workspaces.png "Seznam pracovních prostorů")

1. Pokud musíte změnit právnickou osobu (společnost), klepněte na tlačítko Nabídka (někdy označované jako hamburger nebo hamburgerové tlačítko) v levém horním rohu a poté klepněte na **Změnit společnost**.

    ![Změna právnické osoby.](media/mobile-app-change-comp.png "Změna právnické osoby.")

1. Na stránce **Pracovní prostory** vyberte pracovní prostor, se kterým chcete pracovat, a otevřete jej.

    ![Mobilní pracovní prostor správy majetku](media/mobile-app-asset-workspace.png "Mobilní pracovní prostor správy majetku")

## <a name="work-with-the-asset-management-mobile-workspace"></a>Práce s mobilním pracovním prostorem správy majetku

Další informace o tom, jak pracovat s mobilním pracovním prostorem **Správa majetku**, získáte v tématu [Použití mobilního pracovního prostoru Správa majetku](asset-management-mobile-workspace.md).

Více informací o mobilní aplikaci Finance and Operations (Dynamics 365) získáte v tématu [Domovská stránka mobilní aplikace](../../fin-ops-core/dev-itpro/mobile-apps/Mobile-app-home-page.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]