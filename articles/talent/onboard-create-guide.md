---
title: Vytvoření a odeslání průvodce zaškolením za použití Dynamics 365 Talent - Onboard
description: V tomto tématu je vysvětleno, jak pomocí aplikace Microsoft Dynamics 365 Talent - Onboard vytvořit průvodce zaškolením pro nové zaměstnance. Tento úkol je zásadním prvním krokem strategie pro nakládání s lidským kapitálem (HCM).
author: andreabichsel
manager: ''
ms.date: 05/02/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: HcmCourseType, HcmCourseTypeGroup, HRMCourseTable
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-05-06
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 2371d86165390503312c2848842acf4745a8ed7a
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/06/2019
ms.locfileid: "2898241"
---
# <a name="create-and-send-an-onboarding-guide"></a>Vytvoření a odeslání průvodce zaškolením

[!include [banner](includes/banner.md)]

Aplikace Microsoft Dynamics 365 Talent: Onboard umožňuje vytvářet průvodce zaškolením na základě šablon, které jste vytvořili sami, z šablon, které jsou k dispozici v galerii, nebo od začátku.

Jakmile vytvoříte průvodce zaškolením, můžete ji odeslat novému zaměstnanci. Případně jej můžete odeslat více novým zaměstnancům, které zadáte v souboru Microsoft Excel, který stáhnete z aplikace Onboard.

## <a name="create-an-onboarding-guide-from-a-template-and-send-it-to-a-single-new-hire"></a>Vytvořte průvodce zaškolením ze šablony a odešlete ji jedinému novému zaměstnanci

1. V levé nabídce vyberte možnost **Šablony**.
2. V části **Moje šablony** vyberte šablonu, kterou chcete nastavit jako průvodce zaškolením pro nového zaměstnance.
3. Podle potřeby upravte šablonu. Nezapomeňte si pravidelně ukládat svou práci.
4. Po dokončení úprav šablony vyberte možnost **Vytvořit průvodce**.

    [![Vytvoření průvodce zaškolením ze šablony.](./media/onboard-create-guide.png)](./media/onboard-create-guide.png)

5. V okně **Vytvořit průvodce**, které je v sekci **Koho zaškolujete?**, zadejte jméno nebo e-mailovou adresu nového zaměstnance. Pokud nový zaměstnanec není dosud v systému, vyberte možnost **Přidat nyní** a zadejte informace o daném zaměstnanci.

    ![[Zadání údajů pro průvodce zaškolením](./media/onboard-create-a-guide-window.png)](./media/onboard-create-a-guide-window.png)

6. V části **Kdy začínají?** vyberte počáteční datum.
7. Má-li být průvodce zaškolením automaticky odeslán novému zaměstnanci k určitému datu, ujistěte se, že je zaškrtnuta možnost **Naplánovat datum automatického odeslání** a vyberte datum automatického odeslání. Chcete-li průvodce odeslat okamžitě, vypněte možnost **Naplánovat datum automatického odeslání**.
8. Vyberte **Hotovo**.
9. Po dokončení úprav průvodce zaškolení vyberte možnost **Odeslat** v pravém horním rohu. Potom proveďte jeden z následujících kroků:

    - Chcete-li odeslat novému zaměstnanci odkaz na průvodce zaškolením, vyberte možnost **Kopírovat odkaz** a poté vyberte **Kopírovat**.
    - Chcete-li před odesláním upravit e-mailovou zprávu s průvodcem zaškolením, vyberte **Přizpůsobte si e-mail před jeho odesláním**, vyberte **Další**, přizpůsobte e-mail požadovaným způsobem a pak vyberte možnost **Odeslat**.
    - Chcete-li odeslat e-mail bez jeho přizpůsobení, vyberte možnost **Další** a pak vyberte **Odeslat**.

## <a name="create-an-onboarding-guide-from-a-template-and-send-it-to-multiple-new-hires"></a>Vytvořte průvodce zaškolením ze šablony a odešlete jej více novým zaměstnancům

Onboard vám umožňuje odeslat průvodce zaškolením několika novým zaměstnancům současně.

1. V levé nabídce vyberte možnost **Šablony**.
2. V části **Moje šablony** vyberte šablonu, kterou chcete nastavit jako průvodce zaškolením pro nové zaměstnance.
3. Podle potřeby upravte šablonu. Nezapomeňte si pravidelně ukládat svou práci.
4. Po dokončení úprav šablony vyberte možnost **Vytvořit průvodce**.
5. V okně **Vytvořit průvodce** vyberte možnost **Potřebujete zaškolit více lidí najednou**.

    [![Vytvoření průvodce zaškolením pro více nových zaměstnanců](./media/onboard-send-guide-multiple-people.png)](./media/onboard-send-guide-multiple-people.png)

6. Vyberte **šablonu nového zaměstnance**.
7. Po stažení souboru .xlsx vyberte možnost **Otevřít**, zadejte informace o zaměstnancích do sešitu aplikace Excel a sešit uložte.

    [![Probíhá stahování šablony aplikace Excel pro odeslání průvodce zaškolením více novým zaměstnancům](./media/onboard-send-guide-download-spreadsheet.png)](./media/onboard-send-guide-download-spreadsheet.png)

    > [!NOTE]
    > Před úpravou sešitu je nutné vybrat možnost **Povolit úpravy** v aplikaci Excel.
    > 
    > [![Povolit úpravy](./media/onboard-send-guide-enable-editing.png)](./media/onboard-send-guide-enable-editing.png)

8. Přetáhněte sešit aplikace Excel do vymezené oblasti v okně **Vytvořit více průvodců** nebo klepnutím na libovolné místo v této oblasti vyhledejte soubor v počítači.

    [![Přetažení upraveného sešitu](./media/onboard-send-guide-drag-spreadsheet.png)](./media/onboard-send-guide-drag-spreadsheet.png)

9. Po dokončení úprav průvodce zaškolení vyberte možnost **Odeslat** v pravém horním rohu. Potom proveďte jeden z následujících kroků:

    - Chcete-li odeslat novým zaměstnancům odkaz na průvodce zaškolením, vyberte možnost **Kopírovat odkaz** a poté vyberte **Kopírovat**.
    - Chcete-li před odesláním upravit e-mailovou zprávu s průvodcem zaškolením, vyberte **Přizpůsobte si e-mail před jeho odesláním**, vyberte **Další**, přizpůsobte e-mail požadovaným způsobem a pak vyberte možnost **Odeslat**.
    - Chcete-li odeslat e-mail bez jeho přizpůsobení, vyberte možnost **Další** a pak vyberte **Odeslat**.

## <a name="create-a-guide-without-using-a-template"></a>Vytvořit průvodce bez použití šablony

Není vždy nutné vytvářet průvodce ze šablony. Chcete-li, můžete místo toho vytvořit průvodce od začátku.

1. V levé nabídce vyberte možnost **Průvodce** a poté vyberte tlačítko **Přidat** (znaménko plus \[**+**\]).
2. V okně **Vytvořit průvodce**, které je v sekci **Koho zaškolujete?**, zadejte jméno nebo e-mailovou adresu nového zaměstnance. Pokud nový zaměstnanec není dosud v systému, vyberte možnost **Přidat nyní** a zadejte informace o daném zaměstnanci.

    ![[Zadání údajů pro průvodce zaškolením](./media/onboard-create-a-guide-window.png)](./media/onboard-create-a-guide-window.png)

3. V části **Kdy začínají?** vyberte počáteční datum.
4. Má-li být průvodce zaškolením automaticky odeslán novému zaměstnanci k určitému datu, ujistěte se, že je zaškrtnuta možnost **Naplánovat datum automatického odeslání** a vyberte datum automatického odeslání. Chcete-li průvodce odeslat okamžitě, vypněte možnost **Naplánovat datum automatického odeslání**.
5. Vyberte **Hotovo**.

## <a name="save-a-guide-as-a-template"></a>Uložit průvodce jako šablonu

Průvodce zaškolením můžete uložit jako šablonu. Tímto způsobem můžete ušetřit čas, když musíte později vytvořit další průvodce.

1. V levé nabídce vyberte možnost **Průvodci**.
2. Vyberte tlačítko **Více** (tři tečky \[**...**\]) pro průvodce, ze kterého chcete vytvořit šablonu, a poté vyberte možnost **Uložit jako šablonu**.

    ![[Uložení průvodce zaškolením jako šablonu.](./media/onboard-save-guide-as-template.png)](./media/onboard-save-guide-as-template.png)

3. V okně **Uložit jako novou šablonu** zadejte název nové šablony a pak vyberte možnost **Uložit**.

## <a name="next-steps"></a>Další kroky

- [Úprava průvodců a šablon zaškolení](./onboard-edit-guides-templates.md)
- [Sdílení obsahu s jinými přispěvateli](./onboard-share-template.md)
- [Zobrazit stav úkolů a zaškolení zaměstnanců](./onboard-view-status.md)
- [Vytvořit náborové týmy v Onboard](./onboard-create-team.md)

### <a name="see-also"></a>Viz také

- [Vyzkoušejte nebo kupte aplikaci Onboard](https://dynamics.microsoft.com/talent/onboard/)
- [Co je nového a co se změnilo v aplikaci Dynamics 365 Talent](./whats-new.md)
- [Plány vydání](https://docs.microsoft.com/business-applications-release-notes/index)
- [Získání podpory pro Microsoft Dynamics 365 Talent](./talent-support.md)
