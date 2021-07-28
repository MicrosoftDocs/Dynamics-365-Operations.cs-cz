---
title: Nastavení Elektronické fakturace
description: Toto téma poskytuje informace o nastavení elektronické fakturace v Microsoft Dynamics 365 Finance a Dynamics 365 Supply Chain Management.
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
ms.openlocfilehash: 35a2abaa2165288097bc07b47320e002efc290e7
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/06/2021
ms.locfileid: "6348479"
---
# <a name="set-up-electronic-invoicing"></a>Nastavení Elektronické fakturace

[!include [banner](../includes/banner.md)]


Nastavení funkce elektronické fakturace je proces vytváření požadované konfigurace prostřednictvím prostředí Regulatory Configuration Services (RCS) a publikování této konfigurace na server Elektronické fakturace. Nastavení umožňuje vytvořit konfigurovatelná pravidla, která Elektronické fakturaci umožňují používat zabezpečený protokol přes internet ke komunikaci a výměně dat s entitou třetí strany prostřednictvím webových služeb.

Konfigurovatelnost závisí na konfiguraci formátu Electronic reporting (ER) jako prostředku k vytváření obsahu, který je odesílán a přijímán prostřednictvím digitálních souborů. Také se spoléhá na orchestraci komunikačních akcí k odesílání požadavků a přijímání odpovědí z webových služeb třetích stran, aniž byste museli psát kód.

## <a name="overview"></a>Přehled

„Funkce elektronické fakturace“ je obecný název prostředku, který je nakonfigurován a publikován tak, aby využíval server Elektronické fakturace. Nastavení funkce mimo jiné kombinuje použití konfiguračních formátů elektronických zpráv (ER) k vytvoření konfigurovatelných souborů exportu a importu a použití akcí a toků akcí k umožnění vytváření konfigurovatelných pravidel pro odesílání požadavků, import odpovědi a analýzu obsahu odpovědí.

Následující obrázek ukazuje hlavní součásti funkce elektronické fakturace.

![Přehled funkce elektronické fakturace.](media/e-Invoicing-services-feature-setup-Overview-e-Invoicing-feature.png)

Z důvodu variací formátů faktur a toků akcí se může nastavení funkce lišit podle země nebo oblasti nebo podle obchodních požadavků.

## <a name="set-up-the-electronic-invoicing-feature"></a>Nastavení funkce elektronické fakturace

Proces instalace musí být dokončen ve vašem prostředí RCS. Podle těchto pokynů vytvořte novou funkci elektronické fakturace.

1. Přihlaste se k prostředí RCS.
2. V pracovním prostoru **Funkce globalizace** v části **Funkce** vyberte dlaždici **Elektronická fakturace**.
3. Na stránce **Funkce elektronické fakturace** vyberte **Import**, chcete-li importovat konfiguraci datového modelu ER z globálního úložiště.
4. Vyberte **Přidat**, chcete-li vytvořit funkci elektronické fakturace. Funkci můžete vytvořit buď úplně od začátku, nebo ji odvodit ze stávající funkce elektronické fakturace.

    ![Přidání funkce elektronické fakturace.](media/e-Invoicing-services-feature-setup-Select-Add-e-Invoicing-feature.png)

> [!NOTE]
> Když vytvoříte novou funkci elektronické fakturace, bude mít číslo verze a její výchozí stav je nastaven na **Koncept**.

### <a name="configurations"></a>Konfigurace

Konfigurace obsahují konfigurace formátu ER, které jsou vyžadovány pro transformace a pro vytváření souborů, které budou vyměňovány během komunikace s webovými službami třetích stran. Funkce elektronické fakturace může mít tolik konfigurací formátu souboru ER, kolik je požadováno, na základě technické specifikace integrace poskytnuté poskytovatelem webových služeb.

Podle těchto pokynů přidejte formáty ER k funkci elektronické fakturace.

1. Na stránce **Funkce elektronické fakturace** na kartě **Konfigurace** vyberte **Přidat**, chcete-li přidat konfigurace formátu souboru ER pro funkci elektronické fakturace.

    ![Přidání konfigurace funkce elektronické fakturace.](media/e-Invoicing-services-feature-setup-Select-Add-e-Invoicing-feature-Configurations.png)

    > [!NOTE]
    > Když vytvoříte funkci elektronické fakturace úplně od začátku, musíte ručně přidat všechny konfigurace formátu souboru ER. Když odvodíte funkci elektronické fakturace z existujícího prvku, automaticky se vytvoří konfigurace formátu souboru ER, protože se dědí z původní funkce elektronické fakturace.

2. Vyberte **Upravit** pro otevření stránky **Návrhář formátů**, kde můžete upravit konfiguraci formátu souboru ER.

    ![Úprava konfigurace funkce elektronické fakturace.](media/e-Invoicing-services-feature-setup-Select-Edit-e-Invoicing-feature-Configurations.png)

    > [!NOTE]
    > Při úpravách formátu je stav konfigurační verze nastaven na **Koncept**.

3. Použijte stránku **Návrhář formátů**, chcete-li změnit konfiguraci formátu souborů. Další informace získáte v tématu [Vytvoření konfigurací elektronického dokumentu](../../fin-ops-core/dev-itpro/analytics/electronic-reporting-configuration.md).

    ![Stránka návrháře formátu.](media/e-Invoicing-services-feature-setup-ER-Format-designer.png)

### <a name="feature-setups"></a>Nastavení funkcí

Nastavení funkcí zapouzdřují pravidla pro komunikaci a zabezpečení s webovou službou třetí strany. Funkce elektronické fakturace může mít tolik nastavení funkcí, kolik je požadováno, na základě obchodního pravidla, které chcete dosáhnout.

Podle těchto pokynů přidejte nastavení funkce k funkci elektronické fakturace.

1. Na stránce **Funkce elektronické fakturace** na kartě **Nastavení** vyberte **Přidat**, chcete-li přidat nastavení funkcí pro funkci elektronické fakturace.

    ![Přidání nastavení funkce elektronické fakturace.](media/e-Invoicing-services-feature-setup-Select-Add-e-Invoicing-feature-Setups.png)

    > [!NOTE]
    > Když vytvoříte funkci elektronické fakturace úplně od začátku, musíte ručně přidat všechny požadované nastavení funkcí. Když odvodíte funkci elektronické fakturace z existujícího prvku, automaticky se vytvoří všechna nastavení funkcí, protože se dědí z původní funkce elektronické fakturace.

2. Vyberte **Upravit**, chcete-li upravit nastavení verze funkce.

    ![Úprava nastavení funkce elektronické fakturace.](media/e-Invoicing-services-feature-setup-Select-Edit-e-Invoicing-feature-Setups.png)

3. Použijte stránku **Nastavení verze funkce** pro konfiguraci akcí, pravidel použitelnosti a proměnných.

    ![Akce, pravidla použitelnosti a proměnné.](media/e-Invoicing-services-feature-setup-View-Actions-Applicability-Rules-Variables.png)

### <a name="actions"></a>Akce

Akce jsou předdefinovaný seznam operací, které jsou spouštěny v sekvenčním pořadí. Tento seznam představuje rozpis kroků, které jsou nutné pro úplné provedení funkce elektronické fakturace. Akce mohou zapouzdřit ve stejné funkci elektronické fakturace komunikaci v obou směrech: odeslání požadavku na cíl a přijetí odpovědi a analýza jeho obsahu.

Každá akce obsahuje předdefinovaný seznam parametrů, které jsou vyžadovány, aby akce splnila svůj účel. Volitelně mohou být poskytnuty další parametry.

#### <a name="actions-fasttab"></a>Pevná záložka Akce

Na stránce **Nastavení verzí funkcí** na kartě **Akce** na pevné záložce **Akce** při správě akcí postupujte podle jednoho nebo obou z těchto kroků:

- Vyberte **Nový** nebo **Vymazat**, chcete-li přidat nové akce nebo odstranit stávající akce.
- Vyberte **Nahoru** nebo **Dolů**, chcete-li přesunout vybrané akce nahoru nebo dolů v mřížce, a proto změnit pořadí, ve kterém jsou spuštěny. Akce se spouštějí v pořadí, v jakém se zobrazují v mřížce, zeshora dolů.

![Správa akcí.](media/e-Invoicing-services-feature-setup-Manage-Actions.png)

V následující tabulce jsou popsána pole, která jsou k dispozici na pevné kartě **Akce**.

| Pole        | popis |
|--------------|-------------|
| Akce       | K dispozici je osm předdefinovaných akcí:<ul><li><strong>Podepsat dokument</strong></li><li><strong>FileStoreActionName</strong></li><li><strong>Převod dokumentu</strong></li><li><strong>Odezva procesu</strong></li><li><strong>Volejte webovou službu REST</strong></li><li><strong>Volejte mexickou službu PAC</strong></li><li><strong>Volejte brazilskou službu SEFAZ</strong></li><li><strong>Volejte italskou službu SDI</strong></li></ul> |
| Název akce  | Název akce a její příkaz k provedení. |
| popis  | Popis akce. |
| Povolit opakování | Vybrané zaškrtávací políčko označuje, že akci lze opakovat, pokud předchozí pokus nebude úspěšný. |
| Opakovat akci | V případě opakování akce, ze které je zahájeno opakování. Opakování pak končí u aktuální akce (včetně opakování). U akcí, které je mají, parametry **Minimum opakování** a **Maximum opakování** určují minimální počet a maximální počet opakování. |

#### <a name="parameters-fasttab"></a>Pevná záložka Parametry

Pevná záložka **Parametry** uvádí seznam parametrů akce, která je vybrána na pevné záložce **Akce**.

![Pevná záložka Parametry.](media/e-Invoicing-services-feature-setup-View-Actions-Parameters.png)

V následující tabulce jsou popsána pole, která jsou k dispozici na záložce s náhledem **Parametry**.

| Pole       | popis |
|-------------|-------------|
| Jméno        | Předdefinovaný seznam parametrů. Další informace viz sekce [Seznam parametrů podle akce](#list-of-parameters-by-action). |
| popis | Popis parametru. |
| Hodnota       | Hodnota parametru. |

#### <a name="list-of-parameters-by-action"></a>Seznam parametrů podle akce

Dostupné parametry se liší v závislosti na akci, která je vybrána na pevné záložce **Akce**.

###### <a name="action-sign-document"></a>Akce: Podepište dokument

| Parametr                             | popis |
|---------------------------------------|-------------|
| Vstupní soubor                            | Soubor vstupního dokumentu XML, který musí být podepsán pomocí elektronického podpisu. |
| Název certifikátu                      | Název certifikátu v úložišti. |
| Typ podpisu                        | Typ podpisu, který se má použít. |
| Název metody podpisu                 | Název metody podpisu, která se používá ke generování elektronického podpisu. |
| Název metody digestu                    | Metoda digestu, která se používá k vygenerování řetězce digestu v digitálním podpisu. |
| Název metody kanonizace          | Typ způsobu kanonizace použitý pro výpočet hodnoty hash signatury. |
| Název referenčního atributu              | Název atributu, který označuje, kam má být ID odkazu vloženo do prvku podpisu. |
| Název prvku k podpisu               | Název prvku XML v dokumentu, který musí být podepsán pomocí elektronického podpisu. Pokud není zadán žádný prvek, je podepsán kořen dokumentu. |
| Název prvku pro vložení podpisu   | Název prvku XML, kam by měl být vložen vygenerovaný digitální podpis. Pokud není zadán žádný prvek, podpis se vloží do kořenu dokumentu. |
| Soubor XLST s transformací digestu       | Soubor XSLT (Extensible Stylesheet Language Transformations), který obsahuje pravidla transformace digestu ke generování řetězce digestu pro elektronický podpis. |
| Cesta k vložení řetězce digest          | Cesta v **\<elementName\>.\<Attribute.Path\>** Formát místa, kam musí být vložen vygenerovaný řetězec digestu. |
| Umístění čísla certifikátu           | Název prvku a atributu, kam by mělo být uvedeno číslo certifikátu. |
| Umístění údajů o certifikátu          | Název prvku a atributu, kam by měla být vložena data certifikátu (base64). |
| Číslo certifikátu je ve formátu ASCII | Hodnota, která určuje, zda je číslo certifikátu zakódováno ve formátu ASCII. |

###### <a name="action-filestoreactionname"></a>Akce: FileStoreActionName

| Parametr  | popis |
|------------|-------------|
| Vstupní soubor | Vstupní soubor k uložení. |

###### <a name="action-transform-document"></a>Akce: Převod dokumentu

| Parametr                       | popis |
|---------------------------------|-------------|
| Vstupní soubor                      | Zdrojový soubor, který poskytuje data, která musí být spuštěna k akci. |
| Směr                       | Hodnota, která označuje, zda se má použít formát importu nebo formát exportu. |
| ID konfigurace                | Formát, který by měl být spuštěn. |
| Verze konfigurace           | Pokud není zadána žádná konfigurační verze, použije se nejnovější verze. |
| Bod integrace konfigurace | Zdrojový soubor, který poskytuje data do modulu runtime pro vytváření sestav. |

###### <a name="action-process-response"></a>Akce: Odezva procesu

| Parametr                    | popis |
|------------------------------|-------------|
| Vstupní soubor                   | Reakce na analýzu. |
| Seznam konfigurací výkaznictví | Seznam konfigurací, které se používají k analýze odpovědí. |

###### <a name="action-call-rest-web-service"></a>Akce: Volejte webovou službu REST

| Parametr                   | popis |
|-----------------------------|-------------|
| Adresa URL webové služby             | Adresa URL, na kterou se mají odesílat požadavky. |
| Časový limit webového požadavku         | Maximální doba (v milisekundách) čekání na odpověď webové služby. |
| Vyžádejte si typ operace      | Typ operace požadavku HTTP (například **GET**, **POST** nebo **DELETE**). |
| Názvy certifikátu           | Názvy certifikátu. |
| Kódování textu odpovědi      | Očekávané kódování textu odpovědi HTTP, aby bylo možné správně dekódovat. |
| Typ obsahu požadavku HTTP   | Vstup záhlaví typu obsahu požadavku HTTP. |
| Text obsahu požadavku HTTP   | Text požadavku HTTP. (Text může být prázdný.) |
| Hodnoty dotazu na parametr HTTP | Hodnoty dotazu na parametry, které se používají k vyplnění adresy URL s proměnnými parametry. |
| Vyžádejte si trasu               | Cesta trasy pro požadavek HTTP. Parametry proměnných lze zapsat v notaci **\{paramName\}**. Zde je příklad: **„api/{id}/submit"**. |
| Seznam parametrů trasy        | Parametry trasy v zápisu klíč – hodnota, které se používají k vložení proměnných do trasy. |
| Vlastní záhlaví HTTP         | Vlastní záhlaví HTTP, která se mají vložit do požadavku. |
| Soubory cookie požadavku HTTP        | Seznam souborů cookie v zápisu klíč – hodnota, které se mají vložit do požadavku záhlaví souborů cookie HTTP. |
| Bezpečnostní protokol           | Bezpečnostní protokol, který se má použít pro požadavky HTTP na komunikaci se serverem. (Ve výchozím se používá nastavení zabezpečení transportní vrstvy \[TLS\] 1.2.) |

###### <a name="action-call-mexican-pac-service"></a>Akce: Volejte mexickou službu PAC

| Parametr                | popis |
|--------------------------|-------------|
| Vstupní soubor               | Soubor, který obsahuje data XML, který bude odeslán do webové služby jako vstupní parametr metody. |
| Adresa URL              | Adresa webové služby (koncový bod). |
| Název webové metody (akce) | Název webové metody (akce), kterou je třeba spustit. |
| Certifikáty             | Řetěz certifikátů, který je vyžadován pro ověření klienta webovou službou. Certifikát klienta by měl být posledním certifikátem v řetězci. Kořenové a zprostředkující certifikáty by měly být první. |
| Časový limit webového požadavku      | Maximální doba (v milisekundách) čekání na odpověď webové služby. |
| Interval opakování           | Interval mezi pokusy o volání a přijetí odpovědi z webové služby. Pokud není zadán žádný interval, po neúspěšném prvním volání nebudou provedeny žádné další pokusy. |
| Počet opakování              | Maximální počet opakovaných pokusů o volání a načtení odpovědi z webové služby. |
| Opakovat do               | Maximální doba (v milisekundách), po kterou mohou pokračovat opětovná volání. |
| Minimální regresní interval         | Minimální sazba regresního intervalu pro exponenciální výpočet intervalů opakování. |
| Maximální regresní interval         | Maximální sazba regresního intervalu pro exponenciální výpočet intervalů opakování. |
| Bezpečnostní protokol        | Bezpečnostní protokol, který se má použít pro požadavky HTTP na komunikaci se serverem. (Ve výchozím nastavení se používá protokol TLS 1.2.) |

###### <a name="action-call-brazilian-sefaz-service"></a>Akce: Volejte brazilskou službu SEFAZ

| Parametr                | popis |
|--------------------------|-------------|
| Vstupní soubor               | Soubor, který obsahuje data XML, který bude odeslán do webové služby jako vstupní parametr metody. |
| Adresa URL              | Adresa webové služby (koncový bod). |
| Název webové metody (akce) | Název webové metody (akce), kterou je třeba spustit. |
| Certifikáty             | Řetěz certifikátů, který je vyžadován pro ověření klienta webovou službou. Certifikát klienta by měl být posledním certifikátem v řetězci. Kořenové a zprostředkující certifikáty by měly být první. |
| Časový limit webového požadavku      | Maximální doba (v milisekundách) čekání na odpověď webové služby. |
| Interval opakování           | Interval mezi pokusy o volání a přijetí odpovědi z webové služby. Pokud není zadán žádný interval, po neúspěšném prvním volání nebudou provedeny žádné další pokusy. |
| Počet opakování              | Maximální počet opakovaných pokusů o volání a načtení odpovědi z webové služby. |
| Opakovat do               | Maximální doba (v milisekundách), po kterou mohou pokračovat opětovná volání. |
| Minimální regresní interval         | Minimální sazba regresního intervalu pro exponenciální výpočet intervalů opakování. |
| Maximální regresní interval         | Maximální sazba regresního intervalu pro exponenciální výpočet intervalů opakování. |
| Bezpečnostní protokol        | Bezpečnostní protokol, který se má použít pro požadavky HTTP na komunikaci se serverem. (Ve výchozím nastavení se používá protokol TLS 1.2.) |

###### <a name="action-call-italian-sdi-service"></a>Akce: Volejte italskou službu SDI

| Parametr                | popis |
|--------------------------|-------------|
| Vstupní soubor               | Soubor, který obsahuje data XML, který bude odeslán do webové služby jako vstupní parametr metody. |
| Adresa URL              | Adresa webové služby (koncový bod). |
| Název webové metody (akce) | Název webové metody (akce), kterou je třeba spustit. |
| Certifikáty             | Řetěz certifikátů, který je vyžadován pro ověření klienta webovou službou. Certifikát klienta by měl být posledním certifikátem v řetězci. Kořenové a zprostředkující certifikáty by měly být první. |
| Časový limit webového požadavku      | Maximální doba (v milisekundách) čekání na odpověď webové služby. |
| Interval opakování           | Interval mezi pokusy o volání a přijetí odpovědi z webové služby. Pokud není zadán žádný interval, po neúspěšném prvním volání nebudou provedeny žádné další pokusy. |
| Počet opakování              | Maximální počet opakovaných pokusů o volání a načtení odpovědi z webové služby. |
| Opakovat do               | Maximální doba (v milisekundách), po kterou mohou pokračovat opětovná volání. |
| Minimální regresní interval         | Minimální sazba regresního intervalu pro exponenciální výpočet intervalů opakování. |
| Maximální regresní interval         | Maximální sazba regresního intervalu pro exponenciální výpočet intervalů opakování. |
| Bezpečnostní protokol        | Bezpečnostní protokol, který se má použít pro požadavky HTTP na komunikaci se serverem. (Ve výchozím nastavení se používá protokol TLS 1.2.) |

### <a name="applicability-rules"></a>Pravidla použitelnosti

Pravidla použitelnosti vám umožňují vytvářet logická pravidla, která určují kontext použití pro nastavení funkce. Shoda mezi kontextem daným obchodním dokumentem, který je odeslán ke zpracování, spolu s kritérii pravidla použitelnosti tedy určuje, která funkce elektronické fakturace se použije ke zpracování tohoto odeslání.

#### <a name="set-up-applicability-rules"></a>Nastavit pravidla použitelnosti

1. Na stránce **Nastavení verze funkce** na kartě **Pravidla použitelnosti** vyberte **Nový**, chcete-li přidat pravidlo použitelnosti.

    ![Správa pravidel použitelnosti.](media/e-Invoicing-services-feature-setup-Manage-Actions-Applicability-rules.png)

2. V mřížce vyberte klauzule, které by měly být seskupeny.
3. Vyberte **Skupinová klazule**.

    ![Seskupení klauzulí.](media/e-Invoicing-services-feature-setup-Manage-Applicability-rules-Group-clause.png)

    Když jsou klauzule seskupeny, je do mřížky přidán nový sloupec. Tento sloupec určuje logický operátor pro seskupené klauzule.

    ![Logický operátor pro seskupené klauzule.](media/e-Invoicing-services-feature-setup-Manage-Applicability-rules-Group-criterias.png)

Chcete-li seskupit klauzule, vyberte seskupené klauzule, jejichž seskupení chcete zrušit, a poté vyberte **Zrušit seskupení klauzulí**.

![Zrušení seskupení klauzulí.](media/e-Invoicing-services-feature-setup-Manage-Applicability-rules-UnGroup-criterias.png)

> [!NOTE]
> Když rušíte seskupení klauzuli, vždy začněte od nejvnitřnější úrovně seskupení.

V následující tabulce jsou popsána pole, která jsou k dispozici na kartě **Pravidla použitelnosti**.

| Pole         | popis |
|---------------|-------------|
| A/nebo        | Logický operátor. |
| Pole         | Pole, které se má použít k vytvoření pravidla. |
| Typ operátora | Typ operátoru:<ul><li>Rovno</li><li>Není rovno</li><li>Větší než / Méně než</li><li>Větší než nebo rovno / menší nebo rovno</li><li>Obsahuje</li><li>Začíná na</li></ul> |
| Hodnota         | Kritérium pravidla. |

### <a name="variables"></a>Proměnné

Můžete vytvořit proměnné a poté je použít jako vstupní hodnotu pro parametr konkrétní akce. Můžete je také použít k výměně informací mezi službami elektronické fakturace a klientem o informace, které jsou výsledkem provedení konkrétní akce v rámci toku odeslání.

#### <a name="set-up-variables"></a>Nastavit proměnné

- Na stránce **Nastavení verze funkce** na kartě **Proměnné** vyberte **Nový** nebo **Vymazat**, chcete-li spravovat proměnné.

    ![Správa proměnných.](media/e-Invoicing-services-feature-setup-Manage-Variables.png)

V následující tabulce jsou popsána pole, která jsou k dispozici na kartě **Proměnné**.

| Pole       | popis |
|-------------|-------------|
| Jméno        | Název proměnné. |
| popis | Stručný popis proměnné. |
| Typ        | Typ proměnné:<ul><li><strong>Konstantní</strong> - Obsah proměnné je neměnný.</li><li><strong>Od klienta</strong> - Obsah proměnné se získává z klienta Microsoft Dynamics 365 během provádění procesu odesílání.</li><li><strong>Klientovi</strong> - Obsah proměnné je zpřistupněn pro import klientem Microsoft Dynamics 365 během provádění procesu odesílání.</li></ul> |
| Datový typ   | Datový typ proměnné:<ul><li>Boolean</li><li>Datum</li><li>Počet</li><li>UUID</li><li>Řetězec</li><li>Soubor</li></ul> |
| Hodnota       | Hodnota proměnné nebo název akce, která nastavuje hodnotu proměnné. |

### <a name="validate-the-feature-setup"></a>Ověřte nastavení funkce

- Na stránce **Nastavení verze funkce** v podokně akcí vyberte **Ověřit** k ověření nastavení verze funkce.

   ![Výběr tlačítka Ověřit.](media/e-Invoicing-services-feature-setup-Select-Validate-Button.png)

Ověření zkontroluje konzistenci celé konfigurace. Například, pokud je konkrétní parametr akce povinný, ale jeho hodnota zůstane prázdná, ověření zjistí tuto nekonzistenci a zobrazí se varování.

## <a name="environments"></a>Prostředí

Prostředí elektronické fakturace musí být přidruženo k funkci elektronické fakturace a musí být pro něj povoleno. Prostředí pro elektronickou fakturaci musí být vytvořena a publikována předem prostřednictvím konfigurace funkcí globalizace v účtu RCS vaší organizace.

Pomocí těchto kroků povolte prostředí elektronické fakturace pro funkci elektronické fakturace.

1. Na stránce **Funkce elektronické fakturace** na kartě **Prostředí** vyberte **Povolit**, chcete-li přidat prostředí elektronické fakturace.
2. V poli **Platí od** zadejte datum, kdy má začít platnost nového prostředí.

![Povolení prostředí elektronické fakturace.](media/e-Invoicing-services-feature-setup-Select-Enable-e-Invoicing-feature-Environment.png)

## <a name="organizations"></a>Organizace

Funkci elektronické fakturace lze sdílet mezi více organizacemi.

- Na stránce **Funkce elektronické fakturace** na kartě **Organizace** vyberte **Sdílet s**, chcete-li přidat organizaci, se kterou chcete sdílet funkci elektronické fakturace.

Chcete-li zastavit sdílení funkce elektronické fakturace s organizací, vyberte **Ukončit sdílení**.

## <a name="versions"></a>Verze

Verze pomáhají řídit životní cyklus funkce elektronické fakturace správou jejího stavu. Můžete vytvořit novou verzi existující funkce elektronické fakturace nebo po dokončení všech konfigurací funkce elektronické fakturace můžete změnit stav funkce na **Dokončeno** a pak na **Publikovat**.

### <a name="create-a-new-version-of-an-existing-electronic-invoicing-feature"></a>Vytvoření nové verze existující funkce elektronické fakturace

1. Na stránce **Funkce elektronické fakturace** v mřížce vlevo vyberte funkci elektronické fakturace.
2. Na kartě **Verze** vyberte **Nová**, chcete-li přidat novou verzi funkce elektronické fakturace.

### <a name="change-the-status-of-the-electronic-invoicing-feature"></a>Změna stavu funkce elektronické fakturace

Podle těchto pokynů spravujte životní cyklus funkce elektronické fakturace.

1. Na stránce **Funkce elektronické fakturace** v mřížce vlevo vyberte funkci elektronické fakturace.
2. Na kartě **Verze** vyberte **Změnit stav** a poté změňte stav z **Koncept** na **Dokončeno**.
3. Zobrazí se výzva k potvrzení, že chcete dokončit funkci elektronické fakturace a všech jejích součástí. Vyberte **Ano** k potvrzení akce nebo **Ne** k jejímu zrušení.

    > [!NOTE]
    > Pokud vyberete **Ano**, automaticky se změní stav konfiguračních verzí, které jsou součástí funkce elektronické fakturace z **Koncept** na **Dokončeno**.

4. Vyberte **Změnit stav** a poté změňte stav z **Dokončeno** na **Publikovat**.
5. Zobrazí se výzva k potvrzení, že chcete publikovat funkci elektronické fakturace a všech jejích součástí v globálním úložišti. Vyberte **Ano** k potvrzení akce nebo **Ne** k jejímu zrušení.

    > [!NOTE]
    > Když vyberete **Ano**, stav konfiguračních verzí se automaticky změní z **Dokončeno** na **Sdílené**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]