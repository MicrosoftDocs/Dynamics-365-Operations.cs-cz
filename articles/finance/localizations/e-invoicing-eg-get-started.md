---
title: Elektronická fakturace pro Egypt
description: Tento článek poskytuje informace, které vám pomohou začít s Elektronickou fakturací pro Egypt v Microsoft Dynamics 365 Finance a Dynamics 365 Supply Chain Management.
author: gionoder
ms.date: 02/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom:
- "97423"
- intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: c2a46ef938c5dee62c0d0acd1648584df344c81a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8904405"
---
# <a name="electronic-invoicing-for-egypt"></a>Elektronická fakturace pro Egypt

[!include [banner](../includes/banner.md)]

Tento článek poskytuje informace, které vám pomohou začít s Elektronickou fakturací pro Egypt. Provede vás konfiguračními kroky, které jsou závislé na zemi ve službě Regulatory Configuration Service (RCS). Tyto kroky doplňují kroky popsané v části [Nastavení elektronické fakturace](e-invoicing-set-up-overview.md).

## <a name="prerequisites"></a>Předpoklady

Než začnete provádět postupy v tomto článku, musejí být dokončeny následující předpoklady:

- Seznamte se s elektronickou fakturací, která je popsána v tématu [Přehled elektronické fakturace](e-invoicing-service-overview.md).
- Přihlaste se do služby RCS a nastavte Elektronickou fakturaci. Další informace naleznete v následujících tématech:

    - [Přihlášení a instalace služby Elektronické fakturace](e-invoicing-sign-up-install.md)
    - [Nastavení zdrojů Azure pro elektronickou fakturaci](e-invoicing-set-up-azure-resources.md)
    - [Nainstalujte doplněk pro mikroslužby ve službě Lifecycle Services](e-invoicing-install-add-in-microservices-lcs.md)
    
- Aktivujte integraci mezi aplikací Microsoft Dynamics 365 Finance nebo Dynamics 365 Supply Chain Management a službou Elektronická fakturace, jak je popsáno v tématu [Aktivace a nastavení integrace s Elektronickou fakturací](e-invoicing-activate-setup-integration.md).
- Vytvořte tajný kód digitálního certifikátu v Azure Key Vault a nastavte jej podle popisu v tématu [Zákaznické certifikáty a tajné kódy](e-invoicing-customer-certificates-secrets.md). Pro účely testování egyptský daňový úřad poskytuje konkrétní testovací digitální certifikáty, které se musí používat pouze během fází testování a ověřování řešení. Další informace najdete na webových stránkách egyptského daňového úřadu pomocí odkazu uvedeného v [SDK egyptské elektronické fakturace](https://sdk.invoicing.eta.gov.eg/faq/).

## <a name="country-specific-configuration-for-the-egyptian-electronic-invoice-eg-feature"></a>Konfigurace specifické pro zemi pro funkci egyptské elektronické fakturace (EG)

Některé parametry funkce **Egyptská elektronická faktura (EG)** jsou publikovány s výchozími hodnotami. Než nasadíte funkci elektronické fakturace do prostředí služby, zkontrolujte a v případě potřeby aktualizujte hodnoty, aby lépe odpovídaly vašim obchodním potřebám.

1. Importujte nejnovější verzi funkce globalizace **Egyptská elektronická faktura (EG)**, jak je popsáno v tématu [Import funkcí z globálního úložiště](e-invoicing-import-feature-global-repository.md).
2. Vytvořte kopii importované funkce globalizace a vyberte pro ni poskytovatele konfigurace, jak je popsáno v tématu [Vytvoření funkce globalizace](e-invoicing-create-new-globalization-feature.md).
3. Na kartě **Verze** ověřte, že je vybrána verze **Koncept**.
4. Na kartě **Nastavení** v mřížce vyberte nastavení funkce **Odvozená prodejní faktura**.
5. Vyberte možnost **Upravit**.
6. Na kartě **Kanál zpracování** vyberte v sekci **Kanál zpracování** možnost **Podepsat dokument JSON pro egyptský daňový úřad**.
7. V sekci **Parametry** vyberte **Název certifikátu** a potom vyberte název digitálního certifikátu, který jste vytvořili.
8. V sekci **Kanál zpracování** vyberte **Integrovat s egyptskou službou ETA**. Tento krok opakujte pro dva výskyty této akce.
9. V sekci **Parametry** vyberte možnosti **Adresa URL webové služby** a **Adresa URL přihlašovací služby**. Poté zkontrolujte parametry adresy URL. Chcete-li získat testovací a produkční adresu URL, přejděte na web egyptského daňového úřadu pomocí odkazu uvedeného v tématu [SDK egyptské elektronické fakturace](https://sdk.invoicing.eta.gov.eg/faq/).
10. Zvolte **Uložit** a zavřete stránku.
11. Opakujte kroky 4 až 10 a nastavte funkci **Odvozená projektová faktura**.

## <a name="country-specific-configuration-for-the-egyptian-electronic-invoice-eg-application-setup"></a>Konfigurace specifické pro zemi pro nastavení aplikace egyptské elektronické fakturace (EG)

Existují parametry, které je nutné nastavit v prostředí Finance nebo Supply Chain Management. Toto nastavení můžete dokončit na dvou místech:

- Přímo v prostředí Finance nebo Supply Chain Management. Více informací viz [Nastavení parametrů Elektronické fakturace](e-invoicing-set-up-parameters.md).
- Ve službě RCS. V rámci nastavení funkce elektronické fakturace můžete definovat všechny parametry a poté je nasadit přímo do prostředí Finance nebo Supply Chain Management při nasazení funkce elektronické fakturace.

U obou možností jsou parametry stejné. Pokud nastavujete svou první funkci ve službě Elektronická fakturace, doporučujeme vám podle následujících kroků nastavit parametry v RCS a poté je nasadit do připojené aplikace.

> [!NOTE]
> Některé verze funkcí elektronické fakturace mohou obsahovat předdefinovanou sadu aplikačních parametrů pro Finance nebo Supply Chain Management. V tomto případě byste měli ověřit správnost údajů. V opačném případě nastavte parametry ručně.

1. Najděte kopii funkce globalizace **Egyptská elektronická faktura (EG)**, kterou jste vytvořili.
2. Na kartě **Verze** ověřte, že je vybrána verze **Koncept**.
3. Na kartě **Nastavení** vyberte **Nastavení aplikace**.
4. V poli **Připojené aplikace** vyberte aplikaci, do které chcete nasadit parametry.
5. Na stránce **Typy elektronických dokumentů** vyberte **Přidat** a vytvořte záznam.
6. V poli **Název tabulky** přidejte **CustInvoiceJour**.
7. V poli **Kontext** přidejte referenci na název mapování **Kontext faktury zákazníka**. Konfigurace se jmenuje **Kontextový model faktury zákazníka**.
8. V poli **Mapování elektronického dokumentu** přidejte referenci na název mapování **Faktura zákazníka**. Konfigurace se jmenuje **Mapování modelu faktury**.
9. Zvolte možnost **Uložit**.
10. Na stránce **Typy odpovědi** vyberte **Přidat**.
11. V poli **Typ odezvy** zadejte **Odpověď**.
12. V poli **Popis** zadejte hodnotu **Zpracovat odpověď**.
13. V poli **Stav odeslání** vyberte **Čeká na zpracování**.
14. V poli **Mapování modelu** vyberte **Import zprávy s odpovědí**. Konfigurace se jmenuje **Import egyptské zprávy s odpovědí (EG)**.
15. Zvolte možnost **Uložit**.
16. Vyberte **přidat**.
17. V poli **Typ odezvy** zadejte **ResponseData**.
18. V poli **Popis** zadejte hodnotu **Zpracovat data odpovědi**.
19. V poli **Stav odeslání** vyberte **Čeká na zpracování**.
20. V poli **Název datové entity** vyberte **SalesInvoiceHeaderV2Entity**.
21. V poli **Mapování modelu** vyberte **Import dat odpovědi**. Konfigurace se jmenuje **Formát importu dat egyptské odpovědi (EG)**.
22. Zvolte **Uložit** a zavřete stránku.
23. Zavřete stránku.

Chcete-li nasadit funkci do prostředí služby a nastavení aplikace do připojené aplikace Finance nebo Supply Chain Management, postupujte podle tématu [Dokončení, publikování a nasazení funkce globalizace](e-invoicing-complete-publish-deploy-globalization-feature.md)

## <a name="privacy-notice"></a>Oznámení o ochraně osobních údajů

Povolení funkce **Egyptská elektronická faktura (EG)** může vyžadovat odesílání omezeného objemu dat. Tato data zahrnují identifikační daňové identifikační číslo organizace. Data budou předána agenturám třetích stran, které byly autorizovány daňovým úřadem pro účely zasílání elektronických faktur tomuto daňovému úřadu v předdefinovaném formátu požadovaném pro integraci s webovými službami těchto vlád. Správce může povolit a zakázat funkci přechodem na **Správa organizace** \> **Nastavení** \> **Parametry elektronického dokumentu**. Na kartě **Funkce** vyberte řádek, který obsahuje funkci **Egyptská elektronická faktura (EG)**, a poté proveďte příslušný výběr. Data importovaná z externích systémů do této online služby Dynamics 365 podléhají našim [Prohlášením o ochraně osobních informací](https://go.microsoft.com/fwlink/?LinkId=512132). Další informace najdete v sekci „Oznámení o ochraně osobních údajů“ v dokumentaci funkcí pro jednotlivé země.

## <a name="additional-resources"></a>Další prostředky

- [Přehled elektronické fakturace](e-invoicing-service-overview.md)
- [Začínáme se správou služby Elektronické fakturace](e-invoicing-get-started-service-administration.md)
- [Začínáme s Elektronickou fakturací](e-invoicing-get-started.md)
- [Elektronické faktury zákazníka v Egyptě](emea-egy-e-invoices.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
