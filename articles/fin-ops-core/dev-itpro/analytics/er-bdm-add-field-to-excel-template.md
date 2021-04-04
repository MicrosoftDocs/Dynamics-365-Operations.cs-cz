---
title: Přidání nových polí do šablony obchodního dokumentu v aplikaci Microsoft Excel
description: Toto téma obsahuje informace o tom, jak přidávat nová pole do šablony obchodního dokumentu v aplikaci Microsoft Excel pomocí funkce správy obchodních dokumentů.
author: NickSelin
manager: AnnBe
ms.date: 11/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERBDWorkspace, ERBDParameters, ERBDTemplateEditor
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-10-01
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: 6368d763f44c015a6e85652b1880cfd86ff5ba09
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/09/2021
ms.locfileid: "5569014"
---
# <a name="add-new-fields-to-a-business-document-template-in-microsoft-excel"></a>Přidání nových polí do šablony obchodního dokumentu v aplikaci Microsoft Excel

[!include[banner](../includes/banner.md)]

Můžete přidat nová pole do šablony, která se používá ke generování obchodních dokumentů ve formátu Microsoft Excel. Tato pole lze přidat jako zástupné symboly, které se používají k vyplňování vygenerovaných dokumentů s požadovanými informacemi z aplikace. U každého přidávaného pole můžete také určit vazbu na zdroje dat a určit, která data aplikace budou zadána do pole v případě, že šablona slouží ke generování obchodních dokumentů.

Chcete-li získat další informace o této funkci, vyplňte příklad tomto tématu. Tento příklad ukazuje, jak aktualizovat šablonu tak, aby vyplnila pole ve vygenerovaných formulářích volných faktur.

## <a name="configure-business-document-management-to-edit-templates"></a>Konfigurace správy obchodních dokumentů k úpravě šablon

Vzhledem k tomu, že je Správa obchodních dokumentů (BDM) sestavena na [přehledu elektronického výkaznictví](general-electronic-reporting.md), musíte před zahájením práce s BDM nakonfigurovat požadované parametry ER a BDM.

1.  Přihlaste se k instanci aplikace Microsoft Dynamics 365 Finance jako správce systému.
2.  Proveďte následující kroky v příkladu v tématu [Přehled správy obchodních dokladů](er-business-document-management.md):

    1.  Proveďte konfiguraci parametrů ER.
    2.  Zapněte BDM.

Nyní můžete začít používat BDM pro úpravy šablon obchodních dokumentů.

## <a name="import-er-solutions-that-contain-a-template"></a>Import řešení ER obsahujících šablonu

Příklad v tomto postupu používá oficiálně publikované řešení ER. Konfigurace ER je nutné importovat do aktuální instance modulu finance.

Konfigurace formátu ER **Volná textová faktura (Excel)** tohoto řešení obsahuje šablonu obchodního dokumentu ve formátu aplikace Excel, který lze upravovat pomocí BDM. Importuje nejnovější verzi této konfigurace formátu ER ze služby Microsoft Dynamics Lifecycle Service (LCS). Odpovídající datové modely ER a konfigurace mapování modelu ER budou importovány automaticky.

Další informace o tom, jak importovat konfigurace elektronického výkaznictví naleznete v tématu [Správa životního cyklu konfigurace elektronického výkaznictví](general-electronic-reporting-manage-configuration-lifecycle.md).

![Stránka Knihovna sdíleného majetku LCS](./media/BDM-AddFldExcel-LCS.png)

### <a name="edit-the-er-solution-template"></a>Úprava šablony řešení ER

1.  Přihlaste se jako uživatel s přístupem do pracovního prostoru **Řízení obchodního dokumentu**.
2.  Otevřete pracovní prostor **Správa obchodních dokumentů**.

    ![Pracovní prostor správy obchodních dokumentů](./media/BDM-AddFldExcel-Workspace.png)

3.  V mřížce vyberte šablonu **Volná textová faktura (Excel)**.
4.  V pravém podokně vyberte možnost **Nová šablona** a vytvořte novou šablonu, která bude založena na vybrané šabloně.
5.  Do pole **Název** zadejte **Volná textová faktura (Excel) Contoso** jako nadpis nové šablony.
6.  Klepnutím na tlačítko **OK** potvrďte zahájení procesu úprav.

Otevře se stránka Editor šablony BDM. V rámci vloženého ovládacího prvku můžete použít Microsoft 365 pro úpravu vybrané šablony online.

![Stránka Editor šablony BDM](./media/BDM-AddFldExcel-EditableTemplate.png)

### <a name="add-the-label-for-a-new-field-to-the-template"></a>Přidání popisku nového pole do šablony

1.  Na stránce editor šablon BDM na pásu karet aplikace Excel zaškrtněte na kartě **Zobrazení** políčka **Záhlaví a mřížky** pro upravitelnou šablonu aplikace Excel.

    ![Zaškrtnutá políčka záhlaví a mřížky](./media/BDM-AddFldExcel-EditableTemplate2.png)

2.  Vyberte buňky **E8:F8**.
3.  Na pásu karet aplikace Excel vyberte na kartě **Domů** položky **Sloučit a vycentrovat** ke sloučení vybraných buněk do nově sloučené buňky **E8:F8**.
4.  Ve sloučené **buňce E8:F8** zadejte **adresu URL**.
5.  Vyberte sloučenou buňku **E7:F7**, vyberte **Kopírovat formát**, pak vyberte sloučenou buňku **E8:F8**, chcete-li ji naformátovat stejným způsobem jako sloučená buňka **E7:F7**.

    ![Popisek nového pole přidaný do šablony](./media/BDM-AddFldExcel-EditableTemplate3.png)

### <a name="format-the-template-to-reserve-space-for-a-new-field"></a>Formátování šablony do vyhrazení místa pro nové pole

1.  Na stránce editor šablon BDM vyberte sloučenou buňku **G8:H8**.
2.  Na pásu karet aplikace Excel vyberte na kartě **Domů** položky **Sloučit a vycentrovat** ke sloučení vybraných buněk do nově sloučené buňky **G8:H8**.
3.  Vyberte sloučenou buňku **G7:H7**, vyberte **Kopírovat formát**, pak vyberte sloučenou buňku **G8:H8**, chcete-li ji naformátovat stejným způsobem jako sloučená buňka **G7:H7**.

    ![Místo rezervované pro nové pole](./media/BDM-AddFldExcel-EditableTemplate4.png)

4.  V poli **Název** vyberte **CompanyInfo**.

    Rozsah **CompanyInfo** aktuální šablony aplikace Excel obsahuje všechna pole, která se používají k vyplnění záhlaví vygenerované sestavy informacemi o aktuální společnosti jako prodávající strany.

    ![Vybraný rozsah CompanyInfo](./media/BDM-AddFldExcel-SelectCompanyInfoRange.png)

### <a name="add-a-new-field-to-the-template"></a>Přidání nového pole do šablony

1.  Na stránce **Editor šablon BDM** v podokně akcí vyberte **Zobrazit formát**.
2.  V podokně **struktura šablony** vyberte možnost **přidat**.

    > [!NOTE]
    > Je nutné upravit část šablony, kterou chcete použít jako nové pole. Tuto úpravu jste již provedli formátováním sloučené buňky **G8: H8**.

    ![Přidání nového pole do šablony](./media/BDM-AddFldExcel-AddCell.png)

3.  Pokud chcete přidat nové pole jako buňku v šabloně, vyberte **Excel\Buňka**.

    Chcete-li do šablony přidat nový rozsah, můžete vybrat **Excel\Rozsah**. Zadaná oblast může obsahovat více buněk. Tyto buňky můžete přidat později.
    
    Všimněte si, že součást šablony **CompanyInfo** je automaticky vybrána v podokně **Struktura šablony**, protože se jedná o nejvíce vhodnou nadřazenou komponentu v aktuální struktuře šablon pro pole, které přidáváte.
    
4.  Do pole **rozsah aplikace Excel** zadejte **CompanyURL_Value**.
5.  Vyberte **OK**.

    ![Pole CompanyURL_Value přidané do struktury šablony](./media/BDM-AddFldExcel-EditableTemplate5.png)

6.  V podokně **Struktura šablony** vyberte tlačítko se třemi tečkami (...) a pak vyberte **Zobrazit vazby**.

    ![Zobrazit vybrané vazby](./media/BDM-AddFldExcel-ShowBindings.png)

    V podokně **struktura šablony** se nyní zobrazují zdroje dat, které jsou k dispozici ve formátu základního ER.

7.  Vyberte **CompanyInfo_Value** jako pole, které chcete svázat se zdrojem dat podkladového formátu ER.
8.  V části **Zdroje dat** podokna **Struktura šablony** rozbalte **Model \> InvoiceBase \> CompanyInfo**.
9.  V části **CompanyInfo** vyberte položku **WebsiteURI**.

    ![Vybraná položka WebsiteURI](./media/BDM-AddFldExcel-BindURL.png)

10. Vyberte možnost **vazba**.
11. V podokně **struktura šablony** vyberte možnost **Uložit** a poté zavřete stránku Editor šablon BDM.

V pracovním prostoru **Správa obchodních dokumentů** se na kartě **šablona** v pravém podokně zobrazí aktualizovaná šablona. V mřížce si povšimněte, že pole **Stav** pro upravenou šablonu bylo změněno na **koncept** a pole **Revize** již není prázdné. Tyto změny označují, že byl zahájen proces úpravy této šablony.

![Upravená šablona v pracovním prostoru Správa obchodních dokumentů](./media/BDM-AddFldExcel-Workspace2.png)

## <a name="review-company-settings"></a>Kontrola nastavení společnosti

1.  Přejděte do části **Správa organizace \> Organizace \> Právnické osoby**.
2.  Na pevné záložce **Kontaktní informace** zkontrolujte, zda je zadána adresa URL společnosti.

![Adresa URL společnosti zadaná na stránce právnické osoby](./media/BDM-AddFldExcel-CompanyInfo.png)

## <a name="generate-business-documents-to-test-the-updated-template"></a>Generování obchodních dokumentů pro otestování aktualizované šablony

1.  V aplikaci změňte společnost na **USMF** a přejděte na **Pohledávky \> Faktury \> Všechny faktury s volným textem**.
2.  Vyberte fakturu **FTI-00000002** a poté vyberte možnost **Správa tisku**.
3.  V levém podokně rozbalte položky **Modul – pohledávky \> Dokumenty \> Volné faktury**.
4.  V části **Volná textová faktura** vyberte úroveň **Původní dokument** k určení rozsahu faktur pro zpracování.
5.  V pravém podokně v poli **Formát sestavy** vyberte pro určenou úroveň dokumentu **volnou textovou fakturu (Excel)**.

    ![Vybraná volná textová šablona (Excel) Contoso](./media/BDM-AddFldExcel-PrintMngtSetting.png)

6.  Stisknutím klávesy **Esc** zavřete aktuální stránku.
7.  Vyberte **Tisk \> Vybrané**.
8.  Stáhněte vygenerovaný dokument a otevřete jej v aplikaci Excel.

    ![Volná textová faktura v aplikaci Excel](./media/BDM-AddFldExcel-PreviewReport.png)

Upravená šablona slouží k vygenerování sestavy volné faktury pro vybranou položku. Chcete-li analyzovat, jak je tato sestava ovlivněna změnami, které jste provedli v šabloně, můžete tuto sestavu spustit v jedné relaci aplikace bezprostředně po změně šablony v jiné relaci aplikace.

## <a name="related-links"></a>Související odkazy

[Přehled elektronického výkaznictví](general-electronic-reporting.md)

[Přehled správy obchodních dokumentů](er-business-document-management.md)

[Návrh konfigurace pro generování sestav ve formátu OPENXML](tasks/er-design-reports-openxml-2016-11.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]