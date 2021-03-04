---
title: Aktualizace struktury šablony obchodního dokumentu
description: Toto téma vysvětluje, jak aktualizovat strukturu šablony obchodního dokumentu pomocí funkce správy obchodních dokumentů.
author: NickSelin
manager: AnnBe
ms.date: 11/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERBDWorkspace, ERBDParameters, ERBDTemplateEditor
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-12-01
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: fd279b28c43e22bec6bf814845fe97828bc96d81
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/05/2020
ms.locfileid: "4681321"
---
# <a name="update-the-structure-of-a-business-document-template"></a>Aktualizace struktury šablony obchodního dokumentu 

[!include[banner](../includes/banner.md)]

V podokně **Struktura šablony** editoru šablon [správy obchodních dokumentů](er-business-document-management.md) můžete upravit šablonu obchodního dokumentu [přidáváním nových polí](er-bdm-add-field-to-excel-template.md) do šablony v aplikaci Microsoft Excel. Struktura šablony je poté automaticky aktualizována v Dynamics 365 Finance, takže odráží změny, které jste provedli v podokně **Struktura šablony**.

Šablonu můžete také upravit pomocí online funkcí aplikací Office 365. Do upravitelného listu můžete například přidat novou pojmenovanou položku, jakou je obrázek nebo tvar. V tomto případě se struktura šablony v aplikaci Finance automaticky neaktualizuje a položka, kterou jste přidali, se nezobrazí v podokně **Struktura šablony**. Aktualizujte strukturu šablony ručně v aplikaci Finance výběrem příkazu **Aktualizovat strukturu** na stránce editoru šablon.

Chcete-li získat další informace o této funkci, dokončete následující příklad.

## <a name="example-update-the-structure-of-a-business-document-template"></a>Příklad: Aktualizace struktury šablony obchodního dokumentu

Tento příklad ukazuje, jak může správce systému aktualizovat strukturu šablony obchodního dokumentu v aplikaci Finance po úpravě šablony v aplikaci Office Online. V následujících částech jsou vysvětleny příslušné kroky.

### <a name="prepare-a-business-document-template-for-editing"></a>Připravte šablonu obchodního dokumentu k úpravám

Proveďte následující procedury v části [Přehled správy obchodních dokumentů](er-business-document-management.md).

1. [Konfigurace parametrů ER](er-business-document-management.md#configure-er-parameters)
2. [Import řešení elektronického výkaznictví](er-business-document-management.md#import-er-solutions)
3. [Povolení správy obchodních dokumentů](er-business-document-management.md#enable-business-document-management)
4. [Konfigurace parametrů](er-business-document-management.md#configure-parameters)

### <a name="edit-a-business-document-template"></a>Úprava šablony obchodního dokumentu

1. V pracovním prostoru **správy obchodních dokumentů** vyberte **Nový dokument**.
2. Na stránce **Vytvořit novou šablonu** vyberte šablonu **Volná faktura (ukázka ER) (Excel)**.
3. Vyberte příkaz **Vytvořit dokument**.
4. Do pole **Název** zadejte **FTI ukázka Litware**.
5. Výběrem **OK** vytvořte novou šablonu.

    > [!NOTE]
    > Pokud jste se ještě nepřihlásili do Office Online, budete [přesměrováni na přihlašovací stránku Office 365](er-business-document-management.md#i-selected-edit-document-but-instead-of-opening-the-bdm-template-editor-page-in-finance-and-operations-i-have-been-sent-to-the-microsoft-365-web-page). Chcete-li se vrátit do prostředí Finance, vyberte tlačítko **Zpět** v prohlížeči.

    Nová šablona se otevře v režimu úprav ve vloženém ovládacím prvku Excel Online na stránce editoru šablon.

[![Použití pracovního prostoru pro správu obchodních dokumentů k úpravám šablony obchodního dokumentu](./media/er-bdm-update-structure1.gif)](./media/er-bdm-update-structure1.gif)

### <a name="review-the-current-structure-of-the-editable-template"></a>Kontrola aktuální struktury upravitelné šablony

1. V aplikaci Excel Online na kartě pásu karet **Zobrazit** vyberte ve skupině **Zobrazit** možnost **Mřížky**.
2. V upravitelné šabloně vyberte obdélník nad názvem šablony. Tento obdélník tvoří obrázek s názvem **rptHeaderCompLogo**.
3. Pokud je skryté podokno **Struktura šablony**, vyberte příkaz **Zobrazit strukturu**.
4. V podokně **Struktura šablony** rozbalte položky **Zpráva \> Faktura \> rptHeader \> rptHeaderPart1**.
5. Všimněte si, že ve struktuře šablon ve Finance je položka **rptHeaderCompLogo** prezentována jako podřízená vůči položce **Zpráva \> Faktura \> rptHeader \> rptHeaderPart1**.

[![Použití pracovního prostoru pro správu obchodních dokumentů ke kontrole aktuální struktury upravitelné šablony](./media/er-bdm-update-structure2.gif)](./media/er-bdm-update-structure2.gif)

### <a name="update-the-structure-of-a-business-document-template-by-deleting-a-picture"></a>Aktualizace struktury šablony obchodního dokumentu odstraněním obrázku

1. V aplikaci Excel Online vyberte v upravitelné šabloně obrázek **rptHeaderCompLogo**.
2. Jedním z následujících kroků odstraňte vybraný obrázek z upravitelné šablony:

    - Stiskněte klávesu **Delete** na klávesnici.
    - Vyberte a podržte na obrázek (nebo na něm klikněte pravým tlačítkem) a poté vyberte možnost **Vyjmout**.

    > [!NOTE]
    > Položka **rptHeaderCompLogo** je aktuálně stále přítomná ve struktuře šablony v aplikaci Finance, přestože obrázek již není součástí šablony aplikace Excel.

3. Výběrem položky **Aktualizovat strukturu** synchronizujte strukturu upravitelné šablony v aplikacích Excel a Finance.
4. V podokně **Struktura šablony** rozbalte položky **Zpráva \> Faktura \> rptHeader \> rptHeaderPart1**.
5. Všimněte si, že položka **rptHeaderCompLogo** již není součástí struktury šablony v aplikaci Finance.

[![Použití pracovního prostoru pro správu obchodních dokumentů k odstranění obrázku z šablony obchodního dokumentu](./media/er-bdm-update-structure3.gif)](./media/er-bdm-update-structure3.gif)

### <a name="update-the-structure-of-a-business-document-template-by-adding-a-picture"></a>Aktualizace struktury šablony obchodního dokumentu přidáním obrázku

1. V aplikaci Excel Online na kartě pásu karet **Vložit** vyberte ve skupině **Ilustrace** možnost **Obrázek**.
2. Zvolte možnost **Vybrat soubor**, přejděte k obrázku, který chcete přidat, vyberte jej a poté vyberte **OK**.
3. Vyberte možnost **Vložit**.
4. Posunujte nový obrázek, dokud nebude na správném místě. Ve výchozím nastavení Excel pojmenuje obrázek. Obrázek může dostat třeba název **Obrázek 2**.
5. Výběrem položky **Aktualizovat strukturu** synchronizujte strukturu upravitelné šablony v aplikacích Excel a Finance.
6. V podokně **Struktura šablony** rozbalte položky **Zpráva \> Faktura \> rptHeader \> rptHeaderPart1**.
7. Všimněte si, že nový obrázek je nyní položkou struktury šablony v aplikaci Finance.

[![Použití pracovního prostoru pro správu obchodních dokumentů k přidání obrázku do šablony obchodního dokumentu](./media/er-bdm-update-structure4.gif)](./media/er-bdm-update-structure4.gif)

## <a name="related-links"></a>Související odkazy

[Přehled elektronického výkaznictví](general-electronic-reporting.md)

[Přehled správy obchodních dokumentů](er-business-document-management.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]