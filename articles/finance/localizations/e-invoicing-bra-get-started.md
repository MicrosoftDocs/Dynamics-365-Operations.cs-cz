---
title: Začínáme s Elektronickou fakturací pro Brazílii
description: Toto téma poskytuje informace, které vám pomohou začít s Elektronickou fakturací pro Brazílii ve Finance a Supply Chain Management.
author: gionoder
ms.date: 03/29/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 82bbf806d207af0b15406e4bec516420db7f2c06
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2022
ms.locfileid: "7984846"
---
# <a name="get-started-with-electronic-invoicing-for-brazil"></a>Začínáme s Elektronickou fakturací pro Brazílii 

[!include [banner](../includes/banner.md)]

Toto téma poskytuje informace, které vám pomohou začít s Elektronickou fakturací pro Brazílii. Toto téma vás provede kroky konfigurace, které jsou závislé na zemi v Regulatory Configuration Services (RCS), a doplní kroky popsané v tématu [Začínáme s Elektronickou fakturací](e-invoicing-get-started.md).

## <a name="country-specific-configuration-for-brazilian-nf-e-br-electronic-invoicing-feature"></a>Konfigurace specifické pro zemi pro funkci brazilské elektronické fakturace NF-e (BR)

Některé parametry z **funkce Elektronická fakturace v Brazílii NF-e (BR)** jsou publikovány s výchozími hodnotami. Než nasadíte funkci elektronické fakturace do prostředí služby, zkontrolujte a v případě potřeby aktualizujte hodnoty, aby lépe odpovídaly vašim obchodním potřebám.

Tato část doplňuje část **Konfigurace nastavení elektronické fakturace specifická pro zemi** v tématu [Začínáme s Elektronickou fakturací](e-invoicing-get-started.md).

1. V RCS v části **Funkce** pracovního prostoru **Funkce globalizace** vyberte dlaždici **Elektronická fakturace**.
2. Na stránce **Funkce elektronické fakturace** ověřte, že je vybrána funkce elektronické fakturace **Brazilský NF-e (BR)**, kterou jste vytvořili.
3. Na kartě **Verze** ověřte, že je vybrána verze **Koncept**.
4. Na kartě **Nastavení** v mřížce vyberte **Odeslat** a poté vyberte **Upravit**.
5. Na kartě **Akce** ve skupině polí **Akce** polí vyberte akci **(Preview) Podepsat dokument XML**.
6. Ve skupině polí **Parametry** vyberte **Název certifikátu** a do pole **Hodnota** zadejte název certifikátu přidruženého k vašemu parametru trezoru klíčů.
7. Na kartě **Akce** ve skupině polí **Akce** polí vyberte akci **(Preview) Zavolat brazilskou službu SEFAZ**.
8. Ve skupině polí **Parametry** vyberte parametr **URL adresa**.
9. V poli **Hodnota** v případě potřeby zkontrolujte a aktualizujte adresu URL webových služeb zveřejněných dokumentací SEFAZ pro váš stát a poté vyberte **Uložit**.
10. Na kartě **Pravidla použitelnosti** ve skupině polí **Nastavení pravidla použitelnosti** zkontrolujte a aktualizujte kritéria pole **Stát** podle potřeby pro stejný stát, na který se odkazuje URL webových služeb.
11. Zvolte **Uložit** a zavřete stránku.
12. Informace o nasazení funkce elektronické fakturace do prostředí služby najdete v části [Začínáme s Elektronickou fakturací](e-invoicing-get-started.md).

## <a name="country-specific-configuration-of-application-setup-for-brazilian-nf-e-br-electronic-invoicing-feature"></a>Konfigurace nastavení aplikace specifické pro zemi pro funkci brazilské elektronické fakturace NF-e (BR)

Před nasazením nastavení aplikace do aplikace připojené k Finance nebo Supply Chain Management proveďte tyto kroky.

Tato část doplňuje část **Konfigurace nastavení aplikace specifická pro zemi** v tématu [Začínáme s Elektronickou fakturací](e-invoicing-get-started.md).

1. V RCS v části **Funkce** pracovního prostoru **Funkce globalizace** vyberte dlaždici **Elektronická fakturace**.
2. Na stránce **Funkce elektronické fakturace** ověřte, že je vybrána funkce elektronické fakturace **Brazilský NF-e (BR)**.
3. Na kartě **Verze** ověřte, že je vybrána verze **Koncept**.
4. Na kartě **Nastavení** vyberte **Nastavení aplikace** a v poli **Připojená aplikace** vyberte aplikaci, kam chcete provést nasazení.
5. V poli **Název tabulky** ověřte, zda je vybráno **Záhlaví fiskálního dokumentu**.
6. Vyberte **Typy odpovědí** a poté vyberte **Nový**.
7. Do pole **Typ odpovědi** zadejte „Odpověď“ jako pevnou hodnotu a do pole **Popis** do pole zadejte „Popis“.
8. V poli **Stav odeslání** vyberte **Čeká na zpracování**.
9. V poli **Mapování modelů** vyberte **Mapování modelu ze zprávy odpovědi** s  **(Náhled) Formát importu zprávy odpovědi** a vyberte **Uložit**.
10. Vyberte **Nový** a do pole **Typ odpovědi** zadejte „ResponseData“ jako pevnou hodnotu a do pole **Popis** do pole zadejte „Popis“.
11. V poli **Stav odeslání** vyberte **Čeká na zpracování**.
12. V poli **Mapování modelů** vyberte **Import dat odpovědí** s  **(Náhled) Formát importu odpovědi NF-e (BR)** a vyberte **Uložit**.
13. Informace o nasazení nastavení aplikace do aplikace připojené k Finance nebo Supply Chain najdete v tématu [Začínáme s Elektronickou fakturací](e-invoicing-get-started.md).

## <a name="country-specific-configuration-for-brazilian-nfs-e-abrasf-curitiba-br-electronic-invoicing-feature"></a>Konfigurace specifické pro zemi pro funkci brazilské elektronické fakturace NFS-e ABRASF Curitiba (BR)

Některé parametry z **funkce Elektronická fakturace v Brazílii NFS-e ABRASF Curitiba (BR)** jsou publikovány s výchozími hodnotami. Než nasadíte funkci elektronické fakturace do prostředí služby, zkontrolujte a v případě potřeby aktualizujte hodnoty, aby lépe odpovídaly vašim obchodním potřebám.

Tato část doplňuje část **Konfigurace nastavení elektronické fakturace specifická pro zemi** v tématu [Začínáme s Elektronickou fakturací](e-invoicing-get-started.md).

1. V RCS v části **Funkce** pracovního prostoru **Funkce globalizace** vyberte dlaždici **Elektronická fakturace**.
2. Na stránce **Funkce elektronické fakturace** ověřte, že je vybrána funkce elektronické fakturace **Brazilský NFS-e ABRASF Curitiba (BR)**, kterou jste vytvořili.
3. Na kartě **Verze** ověřte, že je vybrána verze **Koncept** a na kartě **Nastavení** v mřížce vyberte **Odeslat**.
4. Vyberte **Upravit** a na kartě **Akce** ve skupině polí **Akce** vyberte první výskyt **(Preview) Podepsat dokument XML**.
5. Ve skupině polí **Parametry** vyberte parametr **Název certifikátu**.
6. V poli **Hodnota** do pole zadejte název certifikátu přidruženého k vašemu parametru trezoru klíčů.
7. Ve skupině polí **Akce** vyberte druhý výskyt **(Preview) Dokument Signxml**.
8. Ve skupině polí **Parametry** vyberte parametr **Název certifikátu**.
9. V poli **Hodnota** do pole zadejte název certifikátu přidruženého k vašemu parametru trezoru klíčů.
10. Na kartě **Akce** ve skupině polí **Akce** polí vyberte akci **(Preview) Zavolat brazilskou službu SEFAZ**.
11. Ve skupině polí **Parametry** vyberte parametr **URL adresa**.
12. V poli **Hodnota** v případě potřeby zkontrolujte a aktualizujte adresu URL webových služeb zveřejněných daňovým úřadem města Curitiba a poté vyberte **Uložit**.
13. Na kartě **Nastavení** v mřížce vyberte **Dotázat** a poté vyberte **Upravit**.
14. Na kartě **Akce** ve skupině polí **Akce** polí vyberte akci **(Preview) Zavolat brazilskou službu SEFAZ**.
15. Ve skupině polí **Parametry** vyberte parametr **URL adresa**.
16. V poli **Hodnota** v případě potřeby zkontrolujte a aktualizujte adresu URL webových služeb zveřejněných daňovým úřadem města Curitiba.
17. Zvolte **Uložit** a pak zavřete stránku.
18. Informace o nasazení funkce elektronické fakturace do prostředí služby najdete v části [Začínáme s Elektronickou fakturací](e-invoicing-get-started.md).

## <a name="country-specific-configuration-of-application-setup-for-brazilian-nfs-e-abrasf-curitiba-br-electronic-invoicing-feature"></a>Konfigurace nastavení aplikace specifické pro zemi pro funkci brazilské elektronické fakturace NFS-e ABRASF Curitiba (BR)

Před nasazením nastavení aplikace do aplikace připojené k Finance nebo Supply Chain Management proveďte tyto kroky.

Tato část doplňuje část **Konfigurace nastavení aplikace specifická pro zemi** v tématu [Začínáme s Elektronickou fakturací](e-invoicing-get-started.md).

1. V RCS v části **Funkce** pracovního prostoru **Funkce globalizace** vyberte dlaždici **Elektronická fakturace**.
2. Na stránce **Funkce elektronické fakturace** věřte, že je vybrána funkce elektronické fakturace **Brazilský NFS-e ABRASF Curitiba (BR)**.
3. Na kartě **Verze** ověřte, že je vybrána verze **Koncept** a na kartě **Nastavení** v mřížce vyberte **Nastavení aplikace**.
4. V poli **Připojená aplikace** vyberte aplikaci, kterou chcete nasadit.
5. V poli **Název tabulky** ověřte, zda je vybráno záhlaví fiskálního dokumentu.
6. Vyberte **Typy odpovědí** a vyberte **Nový**.
7. Do pole **Typ odpovědi** zadejte „ABRASFCuritibaSubmitResponse“ jako pevnou hodnotu a do pole **Popis** do pole zadejte „Popis“.
8. V poli **Stav odeslání** vyberte **Čeká na zpracování**.
9. V poli **Mapování modelů** vyberte **Import zprávy odpovědí** s  **(Preview) Importu zprávy odpovědi NFS-e ABRASF Curitiba (BR)** a vyberte **Uložit**.
10. Vyberte **Nový** a do pole **Typ odpovědi** zadejte „ABRASFCuritibaSubmitResponseData“ jako pevnou hodnotu a do pole **Popis** do pole zadejte „Popis“.
11. V poli **Stav odeslání** vyberte **Čeká na zpracování**.
12. V poli **Mapování modelů** vyberte **Import dat odpovědí** s  **(Náhled) Formát importu odpovědi NFS-e ABRASF (BR)** a vyberte **Uložit**.
13. Vyberte **Nový** a do pole **Typ odpovědi** zadejte „ABRASFCuritibaInquireResponse“ jako pevnou hodnotu a do pole **Popis** do pole zadejte „Popis“.
14. V poli **Stav odeslání** vyberte **Čeká na zpracování**.
15. V poli **Mapování modelů** vyberte **Import zprávy odpovědí** s  **(Preview) Importu zprávy odpovědi NFS-e ABRASF Curitiba (BR)**.
16. Zvolte **Uložit** a zavřete stránku.
17. Informace o nasazení nastavení aplikace do aplikace připojené k Finance nebo Supply Chain najdete v tématu [Začínáme s Elektronickou fakturací](e-invoicing-get-started.md).

## <a name="privacy-notice"></a>Oznámení o ochraně osobních údajů
Povolení funkcí **NF-e Federal – brazilská elektronická faktura (BR)** a **NFS-e – brazilská servisní (městská) elektronická faktura** může vyžadovat zasílání některých dat, včetně identifikačního daňového ID organizace. Tato data budou předána agenturám třetích stran oprávněným daňovým úřadem pro účely zasílání elektronických faktur tomuto daňovému úřadu v předdefinovaném formátu požadovaném pro integraci s webovými službami těchto vlád. Jako správce můžete povolit nebo vypnout funkce **NF-e Federal – brazilská elektronická faktura (BR)** a **NFS-e – brazilská servisní (městská) elektronická faktura**. To lze provést následovně: 

1. Přejděte na **Správa organizace** > **Nastavení** > **Parametry elektronického dokumentu**. 
2. Na kartě **Funkce** vyberte řádek, který obsahuje funkci **NF-e Federal - brazilská elektronická faktura (BR)** nebo **NFS-e - brazilská servisní (městská) elektronická faktura**, a vyberte ji. Data importovaná z těchto externích systémů do této online služby Dynamics 365 podléhají našim [Prohlášením o ochraně osobních informací](https://go.microsoft.com/fwlink/?LinkId=512132). Další informace najdete v oddílech Oznámení o ochraně osobních údajů v dokumentaci funkcí pro jednotlivé země.

## <a name="additional-resources"></a>Další prostředky

- [Přehled elektronické fakturace](e-invoicing-service-overview.md)
- [Začínáme se správou služby Elektronické fakturace](e-invoicing-get-started-service-administration.md)
- [Začínáme s Elektronickou fakturací](e-invoicing-get-started.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
