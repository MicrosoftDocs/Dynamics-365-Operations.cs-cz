---
title: Začínáme s Elektronickou fakturací pro Egypt
description: Toto téma poskytuje informace, které vám pomohou začít s Elektronickou fakturací pro Egypt ve Finance a Supply Chain Management.
author: gionoder
ms.date: 03/29/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: f6175a50a88d2d636bfafc5988265b8657630758
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5840189"
---
# <a name="get-started-with-electronic-invoicing-for-egypt"></a>Začínáme s Elektronickou fakturací pro Egypt

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

Toto téma poskytuje informace, které vám pomohou začít s Elektronickou fakturací pro Egypt. Toto téma vás provede kroky konfigurace, které jsou závislé na zemi v Regulatory Configuration Services (RCS), a doplní kroky popsané v tématu [Začínáme s Elektronickou fakturací](e-invoicing-get-started.md).

## <a name="country-specific-configuration-for-egyptian-electronic-invoice-eg-electronic-invoicing-feature"></a>Konfigurace specifické pro zemi pro funkci egyptské elektronické fakturace (EG)

Některé parametry z **funkce Elektronická fakturace v Egypty (EG)** jsou publikovány s výchozími hodnotami. Než nasadíte funkci elektronické fakturace do prostředí služby, zkontrolujte a v případě potřeby aktualizujte hodnoty, aby lépe odpovídaly vašim obchodním potřebám.

Tato část doplňuje část **Konfigurace nastavení elektronické fakturace specifická pro zemi** v tématu [Začínáme s Elektronickou fakturací](e-invoicing-get-started.md).

### <a name="prerequisites"></a>Předpoklady

Pro provedení procedury v této části musíte:

- Vytvořit tajný klíč digitálního certifikátu, jak je popsáno v části **Vytvoření tajného klíče digitálního certifikátu** sekce v [Začínáme se správou služby elektronické fakturace](e-invoicing-get-started-service-administration.md). Pro účely testování egyptský daňový úřad poskytuje konkrétní testovací digitální certifikáty, které se musí používat pouze během fází testování a ověřování řešení. Další informace najdete na webových stránkách egyptského daňového úřadu pomocí odkazu uvedeného v [SDK egyptské elektronické fakturace](https://sdk.sit.invoicing.eta.gov.eg/faq/).

1. V RCS v části **Funkce** pracovního prostoru **Funkce globalizace** vyberte dlaždici **Elektronická fakturace**.
2. Na stránce **Funkce elektronické fakturace** ověřte, že je vybrána funkce elektronické fakturace **Egyptská elektronická faktura (EG)**, kterou jste vytvořili.
3. Na kartě **Verze** ověřte, že je vybrána verze **Koncept**.
4. Na kartě **Nastavení** v mřížce vyberte nastavení funkce **Prodejní faktura**.
5. Vyberte **Upravit** a na kartě **Akce** ve skupině polí **Akce** vyberte **Podepsat dokument json pro egyptské daňové úřady**.
6. Ve skupině polí **Parametry** vyberte parametr **Název certifikátu** a vyberte název digitálního certifikátu vytvořeného pro použití s funkcí elektronické fakturace.
7. Ve skupině polí **Akce** vyberte **Integrovat s egyptskou službou ETA**. Tento krok opakujte pro dva výskyty této akce.
8. Ve skupině polí **Parametry** polí vyberte **URL webové služby** a **URL přihlašovací služby** a v případě potřeby zkontrolujte parametry adresy URL. Testovací a produkční adresu URL vám sdělí egyptský daňový úřad pomocí odkazu uvedeného v [SDK egyptské elektronické fakturace](https://sdk.sit.invoicing.eta.gov.eg/faq/).
9. Zvolte **Uložit** a zavřete stránku.
10. Informace o nasazení funkce elektronické fakturace do prostředí služby najdete v části [Začínáme s Elektronickou fakturací](e-invoicing-get-started.md).

## <a name="country-specific-configuration-of-the-application-setup-for-the-egyptian-electronic-invoice-eg-electronic-invoicing-feature"></a>Konfigurace nastavení aplikace specifické pro zemi pro funkci egyptské elektronické faktury (EG)

Před nasazením nastavení aplikace do aplikace připojené k Finance nebo Supply Chain Management proveďte tyto kroky.

Tato část doplňuje část **Konfigurace nastavení aplikace specifická pro zemi** v tématu [Začínáme s Elektronickou fakturací](e-invoicing-get-started.md).

1. V RCS v části **Funkce** pracovního prostoru **Funkce globalizace** vyberte dlaždici **Elektronická fakturace**.
2. Na stránce **Funkce elektronické fakturace** ověřte, že je vybrána funkce elektronické fakturace **Egyptská elektronická faktura (EG)**.
3. Na kartě **Verze** ověřte, že je vybrána verze **Koncept**.
4. Na kartě **Nastavení** vyberte **Nastavení aplikace** a v poli **Připojená aplikace** vyberte aplikaci, kam chcete provést nasazení.
5. V poli **Název tabulky** ověřte, zda je vybrán deník faktury zákazníka.
6. Vyberte **Typy odpovědí** a poté vyberte **Nový**.
7. Do pole **Typ odpovědi** zadejte „Odpověď“ a do pole **Popis** do pole zadejte „Popis“.
8. V poli **Stav odeslání** vyberte **Čeká na zpracování**.
9. V poli **Mapování modelů** vyberte **Mapování modelu ze zprávy odpovědi** s  **(Náhled) Formát importu zprávy odpovědi** a vyberte **Uložit**.
10. Vyberte **Nový** a v poli **Typ odpovědí** zadejte „ResponseData“ jako pevnou hodnotu. Zadejte do pole **Popis** „Popis“.
11. V poli **Stav odeslání** vyberte **Čeká na zpracování**.
12. V poli **Název datové entity** vyberte **Záhlaví prodejní faktury V2**.
13. V poli **Mapování modelů** vyberte **Import dat egyptské odpovědi** s  **(Náhled) Formát importu egyptské odpovědi** a vyberte **Uložit**.
14. Informace o nasazení nastavení aplikace do aplikace připojené k Finance nebo Supply Chain Management najdete v tématu [Začínáme s Elektronickou fakturací](e-invoicing-get-started.md).

## <a name="privacy-notice"></a>Oznámení o ochraně osobních údajů

Aktivace funkce **Egyptská elektronická faktra (EG)** může vyžadovat odesílání omezených dat, která zahrnují daňové identifikační číslo organizace. Tato data budou předána agenturám třetích stran oprávněným daňovým úřadem pro účely zasílání elektronických faktur tomuto daňovému úřadu v předdefinovaném formátu požadovaném pro integraci s webovými službami těchto vlád. Správce může povolit a zakázat funkci přechodem na **Správa organizace** > **Nastavení** > **Parametry elektronického dokumentu**. Na kartě **Funkce** vyberte řádek, který obsahuje funkci **Egyptská elektronická faktura (EG)**, a poté proveďte příslušný výběr. Data importovaná z těchto externích systémů do této online služby Dynamics 365 podléhají našim [Prohlášením o ochraně osobních informací](https://go.microsoft.com/fwlink/?LinkId=512132). Další informace najdete v oddílech Oznámení o ochraně osobních údajů v dokumentaci funkcí pro jednotlivé země.

## <a name="additional-resources"></a>Další prostředky

- [Přehled elektronické fakturace](e-invoicing-service-overview.md)
- [Začínáme se správou služby Elektronické fakturace](e-invoicing-get-started-service-administration.md)
- [Začínáme s Elektronickou fakturací](e-invoicing-get-started.md)
- [Elektronické faktury zákazníka v Egyptě](emea-egy-e-invoices.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
