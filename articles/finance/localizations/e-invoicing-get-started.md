---
title: Začněte s doplňkem elektronické fakturace
description: Toto téma poskytuje informace, které vám pomohou začít s doplňkem elektronické fakturace v Microsoft Dynamics 365 Finance a Dynamics 365 Supply Chain Management.
author: gionoder
manager: AnnBe
ms.date: 10/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: e7f58b8a449e056c4718ac6db30dcd0f0623d2a4
ms.sourcegitcommit: 6e0d6d291d4881b16a677373f712a235e129b632
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/08/2020
ms.locfileid: "3971465"
---
# <a name="get-started-with-the-electronic-invoicing-add-on"></a>Začněte s doplňkem elektronické fakturace

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Toto téma poskytuje informace, které vám pomohou začít s doplňkem elektronické fakturace. Nejprve vás provede kroky konfigurace v Microsoft Dynamics Lifecycle Services (LCS), Regulatory Configuration Services (RCS) a Dynamics 365 Finance. Dále popisuje postup pro odesílání dokumentů prostřednictvím služby za použití Dynamics 365 Finance nebo Dynamics 365 Supply Chain Management. Dozvíte se také, jak interpretovat protokoly odeslání.

## <a name="availability"></a>Dostupnost

Doplněk elektronické fakturace je zpočátku k dispozici pro několik zemí. Doplněk podporuje vytváření elektronických faktur a odesílání následujících obchodních dokumentů:

| Země nebo oblast  | Obchodní dokument                          |
|-----------------|--------------------------------------------|
| Rakousko         | Prodejní a projektové faktury                 |
| Belgie         | Prodejní a projektové faktury                 |
| Brazílie          | Elektronický fiskální dokument model 55 (NF-e) |
| Dánsko         | Prodejní a projektové faktury                 |
| Estonsko         | Prodejní a projektové faktury                 |
| Finsko         | Prodejní a projektové faktury                 |
| Francie          | Prodejní a projektové faktury                 |
| Německo         | Prodejní a projektové faktury                 |
| Itálie           | Prodejní a projektové faktury                 |
| Mexiko          | faktura CFDI                               |
| Nizozemsko     | Prodejní a projektové faktury                 |
| Norsko          | Prodejní a projektové faktury                 |
| Španělsko           | Prodejní a projektové faktury                 |
| Evropa          | Prodejní a projektové faktury PEPPOL          |
    
## <a name="licensing"></a>Licence

Doplněk Elektronická fakturace můžete použít s vaší aktuální licencí. K používání služby nejsou vyžadovány žádné další licence.

## <a name="prerequisites"></a>Předpoklady

Před provedením kroků v tomto tématu je třeba splnit následující předpoklady:

- Přístup k vašemu účtu LCS.
- Projekt nasazení LCS, který zahrnuje Finance nebo Supply Chain Management verze 10.0.13 nebo novější.
- Přístup k vašemu účtu RCS.
- Zapněte funkci Globalizace pro svůj účet RCS prostřednictvím modulu **Správa funkcí** . Pro více informací viz [Regulatory Configuration Services (RCS) - funkce globalizace](rcs-globalization-feature.md)
- Vytvořte prostředek trezoru klíčů a účet úložiště Azure. Další informace viz [Vytvořte účet Azure Storage a trezor klíčů](e-invoicing-create-azure-storage-account-key-vault.md).

## <a name="overview"></a>Přehled

Následující obrázek ukazuje pět hlavních kroků, které v tomto tématu provedete.

![Přehled pěti kroků v tomto tématu](media/e-invoicing-services-get-started-overview-5-steps.png)

1. **Nastavení prostředků Azure:** Nakonfigurujte úložiště Azure a nahrávání digitálních certifikátů v trezoru klíčů Azure.
2. **Nastavení LCS:** Nainstalujte doplněk pro mikroslužby.
3. **Nastavení RCS:** Nastavte funkce prostředí, přístupu uživatelů a elektronické fakturace.
4. **Nastavení klienta:** Nastavte spojení mezi klientem a doplňkem elektronické fakturace a vypněte staré funkce pro odesílání a přijímání odpovědí na elektronické dokumenty.
5. **Odeslat faktury:** Odesílejte elektronické dokumenty prostřednictvím doplňku Elektronická fakturace a přijímejte odpovědi.

> [!NOTE]
> Některé konfigurační kroky v tomto tématu jsou společné a nezávislé na zemi / regionu. Kroky a postupy nastavení, které jsou specifické pro zemi / region, jsou popsány v tématech pro jednotlivé země / regiony.

## <a name="lcs-setup"></a>Nastavení LCS

1. Přihlaste se k účtu LCS.
2. Vyberte dlaždici **Správa funkcí Preview** a ve skupině polí **Funkce public preview** vyberte **BusinessDocumentSubmission** .
3. Označte pole **Funkce Preview povolena** .
4. Vyberte projekt nasazení LCS. Než budete moci vybrat projekt, musí být funkční.
5. Na pevné záložce **Doplňky prostředí** vyberte **Nainstalujte nový doplněk** .
6. Vyberte **Odeslání obchodního dokladu** .
7. V dialogovém okně **Instalační doplněk** v poli **ID aplikace AAD** zadejte **091c98b0-a1c9-4b02-b62c-7753395ccabe** . Tato hodnota je pevná hodnota.
8. V poli **ID klienta AAD** zadejte ID účtu předplatného Azure.

    ![Dialogové okno Nastavení doplňku v LCS](media/e-invoicing-services-get-started-lcs-addin-setup.png)

9. Zaškrtnutím políčka přijměte smluvní podmínky.
10. Vyberte **Instalovat** .

## <a name="rcs-setup"></a>Nastavení RCS

Během instalace RCS dokončíte tyto úlohy:

1. Nastavte trezor klíčů v RCS.
2. Nastavte integraci RCS se serverem doplňkové elektronické fakturace.
3. Vytvořte prostředí doplňkové elektronické fakturace pro vaši organizaci.

### <a name="set-up-the-key-vault-in-rcs"></a>Nastavte trezor klíčů v RCS

1. Přihlaste se k účtu RCS.
2. V pracovním prostoru **Funkce globalizace** v části **prostředí** vyberte dlaždici **elektronická fakturace** .
3. Vyberte **Prostředí služeb** .

    ![Výběr Prostředí služeb](media/e-invoicing-services-get-started-select-service-environments.png)

> [!NOTE]
> Možnost **Připojené aplikace** uděluje přístup pro automatickou konfiguraci doplňku elektronické fakturace ve Finance nebo Supply Management prostřednictvím RCS. V současné době je však tato funkce stále ve vývoji.

4. V podokně akcí zvolte **Parametry trezoru klíčů** .

    ![Výběr parametru trezoru klíčů](media/e-invoicing-services-get-started-select-key-vault-parameters.png)

5. V podokně Akce vyberte možnost **Nový** a přidejte trezor klíčů.
6. V poli **URI trezoru klíčů** zadejte hodnotu atributu **Název DNS** prostředku trezoru klíčů, který jste nakonfigurovali v Azure. Informace o tom, kde najít hodnotu **Název DNS** , najdete v části [Vytvořte účet Azure Storage a trezor klíčů](e-invoicing-create-azure-storage-account-key-vault.md).

    ![Pole URI trezoru klíčů](media/e-invoicing-services-get-started-enter-key-vault-uri.png)

7. Na pevné záložce **Certifikáty** vyberte **Přidat** a zadejte názvy všech digitálních certifikátů a tajné kódy z trezoru klíčů, které jsou zapotřebí k navázání důvěryhodných připojení. V poli **Typ** můžete určit, jestli se jedná o certifikát nebo tajný kód. Obě sady hodnot se konfigurují na prostředku trezoru klíčů v Azure.

    ![Přidávání certifikátů](media/e-invoicing-services-get-started-add-digital-certificates.png)

8. Pokud faktura pro vaši zemi / region vyžaduje pro použití digitálního podpisu řetězec certifikátů, vyberte **Řetězec certifikátů** v podokně akcí a poté zadejte sekvenci certifikátů nebo tajných kódů trezoru klíčů, které tvoří řetězec.

### <a name="set-up-the-rcs-integration-with-the-electronic-invoicing-add-on-server"></a>Nastavte integraci RCS se serverem doplňkové elektronické fakturace

1. V pracovním prostoru **Funkce globalizace** v části **Související nastavení** vyberte odkaz **Parametry elektronického výkaznictví** .
2. Vybrat **Kliknutím sem se připojíte ke službě Lifecycle** . Pokud se nechcete připojit k LCS, vyberte **Zrušit** .
3. Na záložce **Služby elektronické fakturace** zadejte do pole **Identifikátor URI koncového bodu služby** hodnotu podle dostupných zeměpisných oblastí: `https://businessdocumentsubmission.us.operations365.dynamics.com/` nebo `https://businessdocumentsubmission.eu.operations365.dynamics.com/`.
4. V poli **ID aplikace** ověřte, zda zobrazuje ID **0cdb527f-a8d1-4bf8-9436-b352c68682b2** . Tato hodnota je pevná hodnota.
5. V poli **ID prostředí LCS** zadejte ID účtu předplatného LCS.

![Zadání doplňkových parametrů elektronické fakturace](media/e-invoicing-services-get-started-enter-e-invoicing-parameters.png)

### <a name="add-an-electronic-invoicing-add-on-environment"></a>Přidejte prostředí doplňku elektronické fakturace

Pro doplněk elektronické fakturace můžete vytvořit různá prostředí, například vývojová, testovací nebo produkční prostředí.

1. V pracovním prostoru **Funkce globalizace** v části **prostředí** vyberte dlaždici **elektronická fakturace** .
2. Vyberte **Nový** pro vytvoření prostředí.
3. V poli **Účet tokenu SAS úložiště** zadejte název tajného kódu trezoru klíčů, který jste nakonfigurovali v trezoru klíčů v RCS.

    ![Pole účtu tokenu úložiště SAS](media/e-invoicing-services-get-started-enter-sas-token-secret.png)

4. Na pevné záložce **Uživatelé** vyberte **Nový** , chcete-li udělit uživatelům přístup k tomuto prostředí.

    ![Přidávání uživatelů služby](media/e-invoicing-services-get-started-enter-service-users.png)

5. V podokně akcí vyberte **Publikovat** , chcete-li publikovat prostředí na serveru doplňku elektronické fakturace.

    ![Tlačítko Publikovat](media/e-invoicing-services-get-started-publish-service-environment.png)

### <a name="e-invoicing-feature-setup"></a>nastavení funkce elektronické fakturace

„Funkce elektronické fakturace“ je obecný název prostředku, který je nakonfigurován a publikován tak, aby využíval server doplňku elektronické fakturace. Nastavení funkce elektronické fakturace mimo jiné kombinuje použití konfiguračních formátů elektronických zpráv (ER) k vytvoření konfigurovatelných souborů exportu a importu a použití akcí a toků akcí k umožnění vytváření konfigurovatelných pravidel pro odesílání požadavků, import odpovědi a analýzu obsahu odpovědí.

Z důvodu variací formátů faktur a toků akcí je nastavení funkce elektronické fakturace závislé na zemi / regionu.

## <a name="set-up-electronic-invoicing-add-on-integration-in-finance-or-supply-chain-management"></a>Nastavte integraci doplňku elektronické fakturace ve Finance nebo Supply Chain Management 

Během tohoto nastavení provedete následující úkoly:

1. Otevřená testovací funkce
2. Chcete-li povolit integraci s Finance, zapněte funkci integrace doplňku elektronické fakturace.
3. Nastavte afdresu URL koncového bodu doplňku elektronické fakturace.
4. Importujte konfigurace ER, které souvisejí s funkcí elektronické fakturace pro konkrétní zemi / region.
5. Zapněte příslušnou funkci elektronické fakturace pro konkrétní zemi / region.
6. Importujte konfigurace ER a nastavte typy odpovědí, které jsou nutné k aktualizaci faktury pro konkrétní zemi / region jako výsledek procesu odeslání.

### <a name="open-flighted-feature"></a>Otevřená testovací funkce
Funkce integrace elektronické faktury je povolena prostřednictvím testování. Testování je koncept, který ve výchozím nastavení umožňuje funkci zapnout nebo vypnout. Následující kroky umožňují testování v neprodukčním prostředí. 

1. ProveĎte následující příkaz SQL:

    INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('BusinessDocumentSubmissionServiceEnabled', 1)
    
    INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('ElectronicInvoicingServiceIntegrationFeature', 1)
    
2. Po provedení výše uvedené změny proveďte IISReset na všech AOS

### <a name="turn-on-the-electronic-invoicing-add-on-integration-feature"></a>Zapněte funkci integrace doplňku elektronické fakturace

1. Přihlaste se k aplikaci Finance nebo Supply Chain Management.
2. V pracovní prostoru **Správa funkcí** vyhledejte novou funkci **Konfigurovatelná integrace doplňku elektronické fakturace** . Pokud se funkce stále nezobrazuje na stránce Správa funkcí, spusťte funkci **Kontrola aktualizací**
3. Vyberte funkci a poté vyberte tlačítko **Povolit nyní** .

### <a name="set-up-the-service-endpoint-url"></a>Nastavte adresu URL koncového bodu služby

1. Přejděte na **Správa organizace \> Nastavení \> Parametry elektronického dokumentu** .
2. Na kartě **Služba odeslání** v poli **Adresa URL koncového bodu služby** zadejte `https://businessdocumentsubmission.us.operations365.dynamics.com/`.
3. V poli **Prostředí** zadejte název prostředí doplňku elektronické fakturace, které jste vytvořili během instalace RCS.

![Zadání parametrů služby](media/e-invoicing-services-get-started-enter-service-endpoint.png)

### <a name="import-the-er-configurations"></a>Import konfigurací ER

Chcete-li povolit shromažďování a odesílání obchodních dat do doplňku elektronické fakturace, musíte importovat datový model ER a konfiguraci datového modelu ER, které souvisejí s funkcí elektronické fakturace pro konkrétní zemi / region, kterou chcete použít.

1. V pracovním prostoru **Elektronické výkaznictví** v části **Poskytovalé konfigurace** vyberte dlaždici **Microsoft** . Ujistěte se, že je tento poskytovatel konfigurace nastaven na **Aktivní** . Další informace o tom, jak nastavit poskytovatele jako **Aktivní** naleznete v tématu [Vytvoření poskytovatelů konfigurací a jejich označení jako aktivních](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11).
3. Vyberte **Úložiště** .
4. Vyberte **Globální prostředek** a potom vyberte **Otevřít** .
5. V dialogovém okně **Připojte se k Lifecycle Services** vyberte **Kliknutím sem se připojíte ke službě Lifecycle** .
6. V závislosti na zemi nebo oblasti, kde chcete použít funkci elektronické fakturace, musíte importovat příslušný datový model, mapování datového modelu a formáty. Informace o konfiguracích ER, které byste měli importovat, najdete v tématu specifické pro zemi / region „Začínáme s doplňkem elektronické fakturace“.
7. Importujte **Kontextový model faktury zákazníka** . Tento model obsahuje další parametry, které mimo jiné popisují prostředí ve Finance, které se používá pro doplněk Elektronická fakturace během zadávání obchodních údajů.

### <a name="turn-on-countryregion-specific-e-invoicing-features"></a><a name="region-specific"></a>Zapněte funkce elektronické fakturace pro konkrétní zemi / region.

Chcete-li zapnout funkce elektronické fakturace specifické pro zemi / region, aby fungovaly s doplňkem elektronické fakturace, musíte tuto funkci zapnout u každé právnické osoby, kde ji chcete použít. Poté již nelze použít starou integraci elektronické fakturace a je zapnuta integrace s novým doplňkem elektronické fakturace.

1. Přejděte na **Správa organizace \> Nastavení \> Parametry elektronického dokumentu** .
2. Na kartě **Funkce** na řádku funkce, která souvisí s funkcí elektronické fakturace specifické pro vaši zemi / region, zaškrtněte políčko ve sloupci **Povoleno** . Informace o tom, které funkce byste měli zapnout, najdete v tématu specifické pro zemi / region „Začínáme s doplňkem elektronické fakturace“.

![Zapnutí funkce elektronické fakturace](media/e-invoicing-services-get-started-enable-invoicing-feature.png)

> [!NOTE]
> Pokud máte více právnických osob, které jsou nakonfigurovány pro různé země nebo regiony, můžete pro každou právnickou osobu zapnout funkci elektronické fakturace specifickou pro danou zemi / region.

### <a name="import-er-configurations-and-set-up-the-response-types-to-update-your-countryregion-specific-invoice-document"></a>Importujte konfigurace ER a nastavte typy odpovědí, abyste mohli aktualizovat fakturační dokument specifický pro vaši zemi / region

Pokud odeslaný fakturační dokument vyžaduje aktualizaci po reakci odeslání na autorizační služby vlády, musíte importovat speciální datový model a konfigurace ER, aby bylo možné aktualizovat stav fakturačního dokladu nebo jakéhokoli jiného dalšího pole.

1. V pracovním prostoru **Elektronické výkaznictví** v části **Poskytovalé konfigurace** vyberte dlaždici **Microsoft** .
2. Vyberte **Úložiště** .
3. Vyberte **Globální prostředek** a potom vyberte **Otevřít** .
4. Importujte **Model zprávy s odpovědí** , **Formát importu zprávy s odpovědí** , **Mapování modelu zprávy s odpovědí na místo určení** a **Formát importu obsahu souboru** .
5. Přejděte na **Správa organizace \> Nastavení \> Parametry elektronického dokumentu** .
6. Na kartě **Elektronický dokument** vyberte **Přidat** k zadání názvu tabulky, která souvisí s fakturačním dokladem specifickým pro vaši zemi / region. Informace o tom, které názvy tabulek byste měli vybrat, najdete v tématu specifické pro zemi / region „Začínáme s doplňkem elektronické fakturace“.
7. Vyberte **Typy odpovědí** , chcete-li konfigurovat typy odpovědí. Informace o tom, které názvy tabulek byste měli vybrat, najdete v tématu specifické pro zemi / region „Začínáme s doplňkem elektronické fakturace“.

![Nastavení typů odpovědí](media/e-invoicing-services-get-started-set-up-response-types.png)

## <a name="e-invoicing-feature-names-by-country"></a>Názvy funkcí elektronické fakturace podle země 
Následující tabulka popisuje další funkce elektronické fakturace, které jsou k dispozici ke stažení z globálního úložiště elektronického výkaznictví za účelem generování elektronických faktur.
V RCS si můžete stáhnout funkce elektronické fakturace uvedené v této tabulce, konfigurace ER a dostupná nastavení funkcí elektronické fakturace.
Ve službě Finance můžete povolit související odkazy na funkce na stránce **Parametry elektronického dokumentu** pro vystavování elektronických faktur pro tyto země. Další informace najdete v části [Zapněte funkce elektronické fakturace specifické pro zemi / region](#region-specific) uvedené dříve v tomto tématu.

| Název funkce                      | popis                                 | Konfigurace ER                                                                                                  | Nastavení                                                                                                                                                         | Země nebo oblast  | Odkaz na funkci      |
|-----------------------------------|---------------------------------------------|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------|------------------------|
| Rakouské elektronické faktury (AT) | Prodejní a projektové faktury pro Rakousko      | - Prodejní faktura OIOUBL <br>- Faktura k projektu OIOUBL <br>- Prodejní dobropis OIOUBL <br>- Dobropis k projektu OIOUBL | - Generování prodejní faktury (AT) <br>- Generování projektové faktury (AT) <br>- Generování prodejního dobropisu (AT) <br>- Generování projektového dobropisu (AT)         | Rakousko         | EUR-00023              |
| Belgická elektronická faktura (BE)   | Prodejní a projektové faktury pro Belgii      | - Prodejní faktura UBL BE <br>- Projektová faktura UBL BE <br>- Dobropis k projektu UBL BE <br>- Prodejní dobropis UBL BE | - Generování prodejní faktury (BE)<br>- Generování projektové faktury (BE) <br>- Generování prodejního dobropisu (BE) <br>- Generování projektového dobropisu (BE)         | Belgie         | EUR-00023              |
| Dánská elektronická faktura (DK)    | Prodejní a projektové faktury pro Dánsko      | - Prodejní faktura OIOUBL <br>- Faktura k projektu OIOUBL <br>- Prodejní dobropis OIOUBL <br>- Dobropis k projektu OIOUBL | - Generování prodejní faktury (DK) <br>- Generování projektové faktury (DK) <br>- Generování prodejního dobropisu (DK)<br>- Generování projektového dobropisu (DK)         | Dánsko         | EUR-00023<br> DK-00001 |
| Nizozemská elektronická faktura (NL)     | Prodejní a projektové faktury pro Nizozemsko  | - Prodejní faktura UBL NL <br>- Projektová faktura UBL NL <br>- Prodejní dobropis UBL NL <br>- Dobropis k projektu UBL NL | - Generování prodejní faktury (NL) <br> - Generování projektové faktury (NL) <br> - Generování prodejního dobropisu (NL) <br>- Generování projektového dobropisu (NL)          | Nizozemsko | EUR-00023              |
| Estonská elektronická faktura (EE)  | Prodejní a projektové faktury pro Estonsko      | - Prodejní faktura (EE) <br> - Projektová faktura (EE)                                                                     | - Generování prodejní faktury (EE) <br>- Generování projektové faktury (EE)                                                                                           | Estonsko         | EUR-00023              |
| Finská elektronická faktura (FI)   | Prodejní a projektové faktury pro Finsko      | - Prodejní faktura (FI) <br>- Generování projektové faktury (FI)                                                          | - Generování prodejní faktury (FI) <br>- Generování projektové faktury (FI)                                                                                           | Finsko         | EUR-00023              |
| Francouzská elektronická faktura (FR)    | Prodejní a projektové faktury pro Francii    | - Prodejní faktura UBL FR <br> - Projektová faktura UBL FR <br> - Prodejní dobropis UBL FR <br>- Dobropis k projektu UBL FR | - Generování prodejní faktury (FR) <br> - Generování projektové faktury (FR) <br>- Generování prodejního dobropisu (FR) <br>- Generování projektového dobropisu (FR)         | Francie          | EUR-00023              |
| Německá elektronická faktura (DE)    | Prodejní a projektové faktury pro Německo      |- Prodejní faktura (DE) <br> - Projektová faktura <DE>                                                                     | - Generování prodejní faktury (DE) <br>- Generování projektové faktury (DE)                                                                                           | Německo         | EUR-00023              |
| Norská elektronická faktura (NO) | Prodejní a projektové faktury pro Norsko       | - Prodejní faktura OIOUBL <br>- Faktura k projektu OIOUBL <br>- Prodejní dobropis OIOUBL <br>- Dobropis k projektu OIOUBL | - Generování prodejní faktury (NO) <br>- Generování projektové faktury (NO) <br>- Generování prodejního dobropisu (NO) <br>- Generování projektového dobropisu (NO)          | Norsko          | EUR-00023<br> NO-00010 |
| Španělská elektronická faktura (ES)   | Prodejní a projektové faktury pro Španělsko        | - Prodejní faktura (ES) <br>- Projektová faktura (ES)                                                                     | - Generování prodejní faktury (ES) <br>- Generování projektové faktury (ES)                                                                                           | Španělsko           | EUR-00023 <br>ES-00025 |
| Italská elektronická faktura (IT)   | Prodejní a projektové faktury pro Itálii        | - (Náhled) Prodejní faktura (IT) <br> - Projektová faktura (IT)                                                           | - Prodejní faktura <br> - Projektová faktura                                                                                                                           | Itálie           | EUR-00023 <br>IT-00036 |
| Elektronická faktura PEPPOL         | Generování prodejní a projektové faktury PEPPOL | - Prodejní faktura PEPPOL <br>- Projektová faktura PEPPOL <br>- Prodejní dobropis PEPPOL <br> - Projektový dobropis PEPPOL | - Generování prodejní faktury PEPPOL <br>- Generování projektové faktury PEPPOL <br>- Generování prodejního dobropisu PEPPOL <br>- Generování projektového dobropisu PEPPOL |                 | EUR-00023              |


## <a name="electronic-invoice-processing-in-finance-and-supply-chain-management"></a>Elektronické zpracování faktur ve Finance a Supply Chain Management

Během zpracování dokončíte tyto úlohy:

1. Odešlete obchodní dokument (fakturu) prostřednictvím doplňku Elektronická fakturace.
2. Zobrazit protokoly provádění podání.

### <a name="submit-business-documents"></a>Odešlete obchodní dokumenty

Během běžného procesu odesílání je komunikace mezi klientem a doplňkem elektronické fakturace obousměrná. Účelem je splnění dvou hlavních úkolů při předkládání elektronických dokumentů:

1. Odešlete všechny elektronické dokumenty, které čekají na odeslání z Finance, a které mají správný stav pro odeslání a splňují kritéria výběru.
2. Importujte do Finance odpověď, kterou doplněk elektronické fakturace vrátí u dříve odeslaných elektronických dokumentů. Po importu se odpovědi analyzují a stav obchodních dokumentů se odpovídajícím způsobem aktualizuje.

Obchodní dokumenty můžete odeslat ručně nebo na základě vašich požadavků na plán.

1. Přejděte na **Správa organizace \> Periodické \> Elektronické dokumenty \> Odesílejte elektronické dokumenty** .
2. Pro první odeslání jakéhokoli dokumentu vždy nastavte možnost **Znovu odeslat dokumenty** na **Ne** . Pokud musíte znovu odeslat dokument prostřednictvím služby, nastavte tuto možnost na **Ano** .
3. Na pevné záložce **Záznamy, které mají být zahrnuty** vyberte **Filtr** a otevřete dialogové okno **Dotaz** , kde můžete vytvořit dotaz pro výběr dokumentů k odeslání.

![Dialogové okno Odeslat elektronické dokumenty](media/e-invoicing-services-get-started-submission-form.png)

### <a name="filter-query"></a>Dotaz filtru

1. V dialogovém okně **Dotaz** na kartě **Rozsah** zadejte kritéria filtru pomocí polí **Tabulka** , **Odvozená tabulka** , **Pole** a **Kritéria** .
2. Vyberte **Přidat** , chcete-li přidat tolik dalších kritérií, kolik potřebujete k výběru obchodních dokumentů.

    ![Nastavení kritérií filtru odeslání](media/e-invoicing-services-get-started-set-up-submission-filter-criteria.png)

3. Zvolte **OK** a zavřete dialogové okno **Dotaz** .
4. Vyberte **OK** a odešlete vybrané obchodní dokumenty do doplňku Elektronická fakturace.

    > [!NOTE]
    > Během prvního pokusu o odeslání dokumentu prostřednictvím služby budete vyzváni k potvrzení spojení s doplňkem Elektronická fakturace. Vyberte **Klikněte zde pro připojení ke službě elektronického odesílání dokumentů** .
    >
    > ![Připojit ke poli zprávy služby elektronického odesílání dokumentů](media/e-invoicing-services-get-started-dialog-form-connect-e-Invoicing-services.png)
    >
    > Pokud je připojení úspěšné, obdržíte potvrzovací zprávu.
    >
    > ![Potvrzení připojení k doplňku Elektronická fakturace](media/e-invoicing-services-get-started-confirmation-connection-e-invoicing-services.png)

5. Zavřete dialogové okno.

> [!NOTE]
> Po každém odeslání centrum akcí zobrazuje počet odeslaných dokumentů.
>
> ![Zprávy centra akcí](media/e-invoicing-services-get-started-view-action-center-messages.png)

### <a name="submission-by-batch"></a>Odesílání po dávkách

Místo ručního odesílání dokumentů můžete automatizovat proces odesílání a spustit jej na pozadí na základě nakonfigurované frekvence dávkového provedení.

1. V dialogovém okně **Odeslat elektronické dokumenty** na pevné záložce **Spustit na pozadí** nastavte u možnosti **Dávkové zpracování** hodnotu **Ano** .
2. Na kartě **Opakování** nakonfigurujte frekvenci dávkového zpracování.

![Nastavení odesílání po dávkách](media/e-invoicing-services-get-started-set-up-submission-batch.png)

### <a name="view-all-submission-logs"></a>Zobrazit všechny protokoly odeslání

1. Přejděte na **Správa organizace \> Periodické \> Elektronické dokumenty \> Protokol o odeslání elektronických dokumentů** .
2. V poli **Typ dokumentu** vyberte typ dokumentu, podle kterého chcete filtrovat.

    ![Výběr typu dokumentu pro zobrazení protokolů odeslání](media/e-invoicing-services-get-started-select-document-type-for-viewing-submission-log.png)

    > [!IMPORTANT]
    > Hodnota, která je uvedena ve sloupci **Stav odeslání** představuje stav, který souvisí s dokončením samotného procesu odesílání. Označuje, zda byl tok akcí nakonfigurovaných v RCS spuštěn až do konce, bez ohledu na to, zda byl elektronický dokument schválen nebo odmítnut. Hodnota ve sloupci **Stav podání** nepředstavuje stav odeslaného dokumentu. Stav odeslaného dokumentu (tj. zda byl dokument schválen nebo zamítnut) si můžete prohlédnout na pevné záložce **Zpracování protokolu akcí** v podrobnostech protokolu odeslání, jak je popsáno dále.

3. V podokně akcí zvolte **Dotazy \> Podrobnosti o odeslání** .
4. Zobrazit podrobnosti protokolu odeslání.

    ![Podrobnosti protokolu odeslání](media/e-invoicing-services-get-started-view-submission-log-form.png)

Výsledky, které se zobrazují v protokolu odeslání, závisí na tom, jak byla v RCS nastavena funkce elektronické fakturace. Bez ohledu na nastavení však protokol odeslání má vždy tři pevné záložky:

- **Zpracování akcí** - tato pevná záložka zobrazí protokol provádění akcí, které jsou konfigurovány ve verzi funkce, která byla nastavena v RCS. Sloupec **Stav** ukazuje, zda byla akce úspěšně spuštěna.
- **Soubory akcí** - tato pevná záložka zobrazí přechodné soubory, které byly vygenerovány během provádění akcí. Můžete vybrat **Zobrazit** a stáhnout soubor a zobrazit jeho obsah.
- **Zpracování protokolu akcí** - Tato pevná záložka zobrazuje výsledky komunikace mezi doplňkem Elektronická fakturace a cílovou webovou službou. Ukazuje také, co bylo vráceno zpracováním webové služby.

## <a name="related-topics"></a>Související témata

- [Přehled doplňku Elektronická fakturace](e-invoicing-service-overview.md)
- [Začněte s doplňkem elektronické fakturace pro Brazílii](e-invoicing-bra-get-started.md)
- [Začněte s doplňkem elektronické fakturace pro Mexiko](e-invoicing-mex-get-started.md)
- [Začněte s doplňkem elektronické fakturace pro Itálii](e-invoicing-ita-get-started.md)
- [Nastavení doplňku Elektronická fakturace](e-invoicing-setup.md)
