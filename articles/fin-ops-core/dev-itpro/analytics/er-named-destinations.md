---
title: Konfigurace cílových míst elektronického výkaznictví pro záznamy pro správu tisku
description: Tento článek vysvětluje, jak konfigurovat cíle závislé záznamech správy tisku elektronického výkaznictví (ER), který je nakonfigurován pro generování odchozích dokumentů.
author: NickSelin
ms.date: 08/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: f3055a27-717a-4c94-a912-f269a1288be6
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2021-08-01
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 2972dc6a0b373cbc63b811c01ef7a5538810edbb
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8872706"
---
# <a name="configure-print-management-record-specific-er-destinations"></a>Konfigurace cílových míst elektronického výkaznictví pro záznamy pro správu tisku

[!include [banner](../includes/banner.md)]

Tento článek vysvětluje, jak může uživatel v roli administrátora systému nebo v role Úředník pohledávek provádět následující úkoly:

- Konfigurovat pojmenované cíle [Elektronického hlášení (ER)](general-electronic-reporting.md) pro řešení ER, které generuje faktury s volným textem.
- Přiřaďte cíl ER k jednomu záznamu [správy tisku](document-reporting-services.md).

Postupy lze provést v rámci společnosti USMF. Není nutné žádné kódování.

## <a name="introduction"></a>Úvod

Můžete konfigurovat [cíle](electronic-reporting-destinations.md) pro každou složku v souboru výstupní komponentu ER [formátu](general-electronic-reporting.md) [konfigurace](general-electronic-reporting.md#Configuration), který se používá pro generování odchozích dokumentů. Když spustíte formát tohoto typu ER a máte příslušná přístupová práva, můžete také změnit nakonfigurované nastavení cíle za běhu.

V Microsoft Dynamics 365 Finance **verze 10.0.17 a novější** může být kód akce [nastaven](er-apis-app10-0-17.md) pro formát ER ke specifikaci akce, kterou uživatelé provedou spuštěním daného formátu ER. Například v modulu **Pohledávky** v nastavení správy tisku můžete vybrat formát ER, který generuje konkrétní obchodní dokument, například fakturu s volným textem. Poté můžete vybrat **Zobrazit** k zobrazení náhledu faktury nebo **Vytisknout** pro odeslání na tiskárnu. Pokud je za běhu předána akce pro spuštěný formát ER, můžete [nakonfigurovat různé cíle ER pro různé akce uživatele](er-action-dependent-destinations.md).

Ve Finance **verze 10.0.21 a novější** pojmenovaný cíl může být [nastaven](er-apis-app10-0-21.md) pro formát ER a přiřazený k záznamu správy tisku, který je zpracován při spuštění tohoto formátu ER. Například v modulu **Pohledávky** v nastavení správy tisku chcete konfigurovat záznam **Originál** a provést následující akce:

- Spustit formát ER.
- Vygenerovanou fakturu odešlete zákazníkovi e-mailem.
- Konfigurujte záznam **Kopírovat** pro spuštění stejného formátu.
- Vytiskněte kopii faktury na síťové tiskárně.

V takovém případě musíte nakonfigurovat různá umístění ER pro spuštěný formát ER a musíte vybrat cíle pro různé záznamy správy tisku.

## <a name="prerequisites"></a>Předpoklady

Než začnete, funkce **Umožnit nastavit cíle ER pro každou položku správy tisku** musí být zapnuta v pracovním prostoru [Správa funkcí](../../fin-ops/get-started/feature-management/feature-management-overview.md#the-feature-management-workspace). Zdrojový kód musí být také změněn, aby bylo možné konfigurovat pojmenované cíle ER v aktuální instanci Finance a povolit [Nové](er-apis-app10-0-21.md) rozhraní API ER.

Navíc konfigurace ER **Faktura s volným textem (Excel)** musí být [importována](er-download-configurations-global-repo.md) do vaší instance Finance.

## <a name="configure-a-new-er-destination"></a>Konfigurace nového cíle ER

1. Přejděte na **Pohledávky** \> **Faktury** \> **Všechny volné faktury**.
2. Vyberte fakturu pro zákaznický účet **US-001**.
3. Na stránce **Faktura s volným textem** na kartě **Faktura** ve skupině **Správa tisku** vyberte **Správa tisku**.
4. Na stránce **Nastavení správy tisku** rozbalte **Modul – pohledávky** \> **Dokumenty** \> **Faktura s volným textem**, vyberte **původní** záznam a pak proveďte následující kroky:

    1.  Sledujte aktuální nastavení vybraného záznamu:
        -   Výchozí sestava SSRS **FreeTextInvoice.Report** je vybrána v poli **Formát zprávy**.
        -   Název **\<Default\>** je uveden v poli **Cíl** a informuje, že pro přiřazenou sestavu SSRS není vybrán žádný vlastní cíl. 
    2.  V poli **Formát zprávy** vyberte konfiguraci formátu ER **Faktura s volným textem (Excel)**.
        -   Název pole **Cíl** se změnil na **Název cíle**.
        -   Název **\<No named destination\>** je uveden v poli **Název cíle** a informuje, že pro přiřazený formát ER není vybrán žádný pojmenovaný cíl.
    3.  Vyberte tlačítko se šipkou vpravo od pole **Název destinace**.    
    4. Na stránce **Pojmenovaný cíl elektronického výkaznictví** v poli **Název** zadejte **Hlavní cíl**.
    5. Zvolte možnost **Uložit**.
    6. Na pevné záložce **Cíl souboru** [konfigurujte](er-destination-type-email.md) cíl **E-mail** pro komponentu **Sestava**.
    7. Zavřete stránku **Pojmenovaný cíl elektronického výkaznictví**.
    8. Na stránce **Nastavení správy tisku** v poli **Název cíle** vyberte pojmenovaný cíl **Hlavní cíl**.

    ![Konfigurace pojmenovaného cíle ER pro vybraný formát ER a jeho přiřazení ke konfigurovanému záznamu správy tisku na stránce nastavení správy tisku](./media/er-named-destinations-01.gif)

    Nyní jste nakonfigurovali pojmenovaný cíl ER **Hlavní cíl** pro formát **Faktura s volným textem (Excel)** a přiřadili jej k **původnímu** záznamu správy tisku v **Modul - pohledávky** \> **Dokumenty** \> **Faktura s volným textem**.

5. Rozbalte **Modul - pohledávky** \> **Účet - US-001** \> **Faktura s volným textem**, vyberte **původní** záznam a poté postupujte takto:

    1. Vyberte a podržte záznam (nebo klikněte pravým tlačítkem) a vyberte možnost **Přepsat**.
    2. Vyberte tlačítko se šipkou vpravo od pole **Název destinace**.
    3. Na stránce **Pojmenovaný cíl elektronického výkaznictví** v podokně akcí vyberte **Nový**.
    4. Do pole **Název** zadejte **Cíl US-001**.
    5. Na pevné záložce **Cíl souboru** [konfigurujte](er-destination-type-print.md) cíl **Tiskárna** pro komponentu **Sestava**.
    6. Zavřete stránku **Pojmenovaný cíl elektronického výkaznictví**.
    7. Na stránce **Nastavení správy tisku** v poli **Název cíle** vyberte pojmenovaný cíl **Cíl US-001**.

    ![Konfigurace pojmenovaného cíle ER pro vybraný formát ER a jeho přiřazení ke konfigurovanému záznamu správy tisku na stránce nastavení správy tisku](./media/er-named-destinations-02.gif)

    Nyní jste nakonfigurovali pojmenovaný cíl ER **Cíl US-001** pro formát **Faktura s volným textem (Excel)** a přiřadili jej k **původnímu** záznamu správy tisku v **Modul - pohledávky** \> **Účet - US-001** \> **Faktura s volným textem**.

Když je nyní zpracována faktura s volným textem, spustí se formát **Faktura s volným textem (Excel)** a dojde k jedné z následujících událostí:

- Pokud je faktura s volným textem pro jiného zákazníka než US-001, je vygenerovaný dokument odeslán e-mailem.
- Pokud je faktura s volným textem pro odběratele US-001, je vygenerovaný dokument vytisknut.

> [!NOTE]
> Pokud pro záznam správy tisku, který je zpracován za běhu, nebylo definováno pojmenované místo určení, použijí se výchozí cíle ER, pokud jsou k dispozici pro formát ER, který je spuštěn.

> [!IMPORTANT]
> Na stránce **Cíl elektronického výkaznictví** (**Správa organizace** \> **Elektronické výkaznictví** \> **Cíl elektronického výkaznictví**), pokud vyberete formát ER, pro který byl nakonfigurován alespoň jeden pojmenovaný cíl, budete upozorněni na přítomnost pojmenovaných cílů.
>
> ![Oznámení o existenci nakonfigurovaných pojmenovaných cílů pro vybraný formát ER na stránce cíle elektronického hlášení](./media/er-named-destinations-03.png)
>
> Pokud odstraníte výchozí cíl, budou odstraněny také všechny pojmenované cíle. Pokud byla tato pojmenovaná místa určení vybrána pro záznamy správy tisku, výběr těchto pojmenovaných cílů se zruší.

## <a name="copy-an-existing-er-destination-as-a-new-named-destination"></a>Zkopírujte stávající cíl ER jako nový pojmenovaný cíl

Pokud je pro formát ER k dispozici výchozí pojmenovaný cíl ER, lze jej použít jako šablonu pro nové cíle ER. Chcete-li vytvořit nový cíl ER, který je založen na výchozím cíli, vyberte **Kopírovat z výchozího nastavení** na stránce **Pojmenovaný cíl elektronického výkaznictví**. Nový cíl je pojmenován jako **Výchozí**. Tento krok můžete opakovat tolikrát, kolikrát je potřeba.

Můžete vybrat jakýkoli existující pojmenovaný cíl jako šablonu pro nový pojmenovaný cíl. Chcete-li vytvořit nový pojmenovaný cíl ER, který je založen na vybraném pojmenovaném cíli, vyberte **Kopírovat** na stránce **Pojmenovaný cíl elektronického výkaznictví**. Nový cíl má stejný název jako zvolený pojmenovaný cíl, ale přidá se přípona „Kopie“. Tento krok můžete opakovat tolikrát, kolikrát je potřeba.

## <a name="security-considerations"></a>Na co brát ohled při zabezpečení

Pojmenované cíle ER můžete nastavit na stránce **Nastavení správy tisku** pouze pokud máte [oprávnění](../sysadmin/role-based-security.md#permissions) k provedení tohoto úkolu. Oprávnění vám může být uděleno, pokud **Nakonfigurujte cíl formátu elektronického hlášení** [povinnost](../sysadmin/role-based-security.md#duties) je přiřazena jedné z vašich [rolí zabezpečení](../sysadmin/role-based-security.md#security-roles). Další informace viz [Na co brát ohled při zabezpečení](electronic-reporting-destinations.md#security-considerations).

## <a name="additional-resources"></a>Další prostředky

[Přehled elektronického výkaznictví](general-electronic-reporting.md)

[Místa určení elektronického výkaznictví](electronic-reporting-destinations.md)

[Změny rozhraní API architektury elektronického výkaznictví pro Application update 10.0.17](er-apis-app10-0-17.md)

[Změny rozhraní API architektury elektronického výkaznictví pro Application update 10.0.21](er-apis-app10-0-21.md)

[Změňte kód, aby uživatelé mohli konfigurovat a používat pojmenované cíle ER](er-api-named-destinations.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
