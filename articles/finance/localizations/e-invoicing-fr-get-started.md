---
title: Začínáme s doplňkem elektronické fakturace pro Francii
description: Tento článek poskytuje informace, které vám pomohou začít s doplňkem elektronické fakturace pro Francii.
author: dkalyuzh
ms.date: 07/07/2022
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2022-00-02
ms.dyn365.ops.version: AX 10.0.29
ms.openlocfilehash: 365316b204b6d76fa6ee6b2402fefee50c8ff3ef
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/02/2022
ms.locfileid: "9220644"
---
# <a name="get-started-with-the-electronic-invoicing-add-on-for-france"></a>Začínáme s doplňkem elektronické fakturace pro Francii

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

Tento článek poskytuje informace, které vám pomohou začít s Elektronickou fakturací pro Francii. Provede vás konfiguračními kroky, které jsou závislé na zemi ve službě Regulatory Configuration Service (RCS). Tyto kroky doplňují kroky popsané v části [Začínáme s doplňkem pro elektronickou fakturací](e-invoicing-get-started.md).

## <a name="country-specific-configuration-for-french-chorus-pro-submission-fr-electronic-invoicing-feature"></a>Konfigurace specifické pro zemi pro funkci francouzské elektronické fakturace Chorus Pro (FR)

Pro konfiguraci funkce elektronické fakturace **Francouzské účtování Chorus Pro (FR)** je třeba provést několik kroků. Některé parametry z konfigurace jsou publikovány s výchozími hodnotami. Tyto hodnoty je třeba zkontrolovat a aktualizovat, aby lépe odrážely vaše obchodní operace.

### <a name="prerequisites"></a>Předpoklady

Než začnete provádět postupy v tomto článku, musejí být dokončeny následující předpoklady:

- Seznámení se s elektronickou fakturací. Další informace získáte v tématu [Přehled elektronické fakturace](e-invoicing-service-overview.md).
- Přihlaste se do služby RCS a nastavte Elektronickou fakturaci. Další informace naleznete v následujících článcích:

    - [Přihlášení a instalace služby Elektronické fakturace](e-invoicing-sign-up-install.md)
    - [Nastavení zdrojů Azure pro elektronickou fakturaci](e-invoicing-set-up-azure-resources.md)
    - [Nainstalujte doplněk pro mikroslužby ve službě Lifecycle Services](e-invoicing-install-add-in-microservices-lcs.md)
    - [Aktivace a nastavení integrace nastavení s elektronickou fakturací](e-invoicing-activate-setup-integration.md) – Použijte informace v tomto článku k aktivaci integrace mezi aplikací Microsoft Dynamics 365 Finance nebo Dynamics 365 Supply Chain Management a službou elektronické fakturace.
    - [NAF kódy a siret čísla](emea-fra-naf-codes-siret-numbers.md) a [Nastavení kódů NAF a čísel Siret](tasks/fr-00003-naf-codes-siret-numbers.md) – Použijte informace v těchto článcích k nastavení kódů NAF a čísel Siret ve vašich právnických osobách. 

- Vaše organizace musí být registrována, aby mohla fungovat ve službě Chorus Pro. Microsoft poskytuje integraci s Chorus pro v režimu OAuth2 prostřednictvím aplikačního programovacího rozhraní (API). Podrobné informace o registraci Chorus Pro a aktivaci aplikace naleznete v [oficiální dokumentaci](https://communaute.chorus-pro.gouv.fr/documentation/help-for-api-developers-in-oauth2-mode/).

    Při registraci u Chorus Pro postupujte takto.

    1. Přejděte na [portál PISTE](https://piste.gouv.fr/en/component/apiportal/registration) pro zahájení registrace. 
    2. Zaregistrujte aplikaci a aktivujte přihlašovací údaje Open Authorization (OAuth).
    3. Zkopírujte a uložte ID klienta přihlašovacích údajů OAuth a tajný klíč. Tyto informace použijete v dalších krocích.
    4. Přejděte na [portál Chorus Pro](https://portail.chorus-pro.gouv.fr/aife_csm/?id=aife_enrollment) k registraci. 
    5. Vytvořte technický účet pro přístup k API. Více informací viz [Vytvoření technického účtu pro přístup k API v produkci](https://communaute.chorus-pro.gouv.fr/documentation/creation-of-a-technical-account-for-an-api-access-in-production/).
    6. Zkopírujte uživatelské ID technického účtu a heslo. Tyto informace použijete v dalších krocích.

## <a name="country-specific-configuration-of-the-application-setup-for-the-french-chorus-pro-submission-fr-electronic-invoicing-feature"></a>Konfigurace nastavení aplikace specifické pro zemi pro funkci francouzské elektronické fakturace Chorus Pro (FR)

Některé parametry funkce elektronické fakturace **Francouzské podání Chorus Pro (FR)** jsou publikovány s výchozími hodnotami. Než nasadíte funkci elektronické fakturace do prostředí služby, zkontrolujte a v případě potřeby aktualizujte hodnoty, aby lépe odpovídaly vašim obchodním potřebám.

1. V Azure Key Vault vytvořte tajné kódy a odpovídající reference na ně. Více informací viz [Zákaznické certifikáty a tajné klíče](e-invoicing-customer-certificates-secrets.md).
2. Importujte nejnovější verzi funkce globalizace **Francouzské podání Chorus Pro (FR)**, jak je popsáno v tématu [Import funkcí z globálního úložiště](e-invoicing-import-feature-global-repository.md).
3. Vytvořte kopii importované funkce globalizace a vyberte poskytovatele konfigurace. Více informací naleznete v tématu [Vytvoření funkce globalizace](e-invoicing-create-new-globalization-feature.md).
4. Na kartě **Verze** ověřte, že je vybrána verze **Koncept**.
5. Na kartě **Nastavení** v mřížce vyberte nastavení funkce **Odvozená prodejní faktura UBL**.
6. Vyberte **Upravit** a poté na kartě **Kanál zpracování** v části **Kanál zpracování** vyberte **(Preview) Integrace s francouzským Chorus Pro** s názvem akce **Francouzské podání Chorus Pro**.
7. V části **Parametry** v poli **Tajný název ID klienta** vyberte tajný název, který jste vytvořili pro ID klienta v trezoru klíčů.
8. V poli **Název tajného klíče klienta** vyberte tajný název, který jste vytvořili pro tajný klíč klienta v trezoru klíčů.
9. V poli **Tajný název technického přihlášení** vyberte tajný název, který jste vytvořili pro přihlášení technického účtu v trezoru klíčů.
10. V poli **Tajný název technického hesla** vyberte tajný název, který jste vytvořili pro přihlášení technického hesla v trezoru klíčů.
11. Na kartě **Kanál zpracování** v části **Kanál zpracování** vyberte **Integrace s francouzským Chorus Pro** s názvem akce **Stav požadavku francouzského Chorus Pro**.
12. V části **Parametry** v poli **Tajný název ID klienta** vyberte tajný název, který jste vytvořili pro ID klienta v trezoru klíčů.
13. V poli **Název tajného klíče klienta** vyberte tajný název, který jste vytvořili pro tajný klíč klienta v trezoru klíčů.
14. V poli **Tajný název technického přihlášení** vyberte tajný název, který jste vytvořili pro přihlášení technického účtu v trezoru klíčů.
15. V poli **Tajný název technického hesla** vyberte tajný název, který jste vytvořili pro přihlášení technického hesla v trezoru klíčů.
16. Zvolte **Uložit** a pak zavřete stránku.
17. Opakujte kroky 6 až 16 pro nastavení funkce **Odvozená faktura projektu UBL**, Nastavení funkce **Odvozený dobropis projektu UBL** a nastavení funkce **Odvozený dobropis projektu UBL**.

## <a name="additional-resources"></a>Další prostředky

- [Přehled doplňku elektronické fakturace](e-invoicing-service-overview.md)
- [Začněte se správou služby doplňku elektronické fakturace](e-invoicing-get-started-service-administration.md)
- [Začněte s doplňkem elektronické fakturace](e-invoicing-get-started.md)
