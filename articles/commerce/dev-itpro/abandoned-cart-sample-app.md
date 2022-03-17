---
title: Detekce opuštěných košíků a zasílání upozornění zákazníkům
description: Toto téma popisuje přizpůsobení ukázkové aplikace konektoru opuštěného košíku Microsoft Dynamics 365 Commerce pro detekci opuštěných košíků a zasílání e-mailových upozornění s připomenutím zákazníkům.
author: bicyclingfool
ms.date: 02/25/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: 82848f1ff068cea0adfc6ec1b33fc4bb035f78dc
ms.sourcegitcommit: 374bbdde90fc9a68c0799158a50409bfbe8ca64e
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/25/2022
ms.locfileid: "8353356"
---
# <a name="detect-abandoned-carts-and-send-notifications-to-customers"></a>Detekce opuštěných košíků a zasílání upozornění zákazníkům

[!include [banner](../includes/banner.md)]

Toto téma popisuje přizpůsobení ukázkové aplikace konektoru opuštěného košíku Microsoft Dynamics 365 Commerce pro detekci opuštěných košíků a zasílání e-mailových upozornění s připomenutím zákazníkům.

Schopnost získat zpět příjmy a udržet si zákazníky prostřednictvím oznámení o opuštěném košíku je důležitou schopností, kterou Dynamics 365 Commerce podporuje. Přizpůsobením ukázkové aplikace konektoru Commerce opuštěného košíku mohou maloobchodníci přistupovat k nákupním košíkům na Serveru maloobchodu, které nebyly změněny během maloobchodníky definovaného časového okna. Tyto košíky lze poté načíst, rozšířit o údaje o produktech a zákaznících a předat je poskytovateli e-mailového marketingu třetí strany, který může generovat e-mailová upozornění a odesílat je zákazníkům.

E-mailové oznámení o opuštěném košíku, které zákazníci obdrží, může obsahovat následující informace:

- Jméno odběratele.
- Příjmení odběratele.
- E-mailovou adresu odběratele.
- Adresu URL, která odběratele vrátí do jeho košíku.
- Měnu transakce.
- Seznam produktů v košíku odběratele. U každého produktu jsou uvedeny následující informace:

    - Zobrazovaný název produktu
    - ID produktu (používá se k sestavení adresy URL vedoucí na stránku s popisem produktu)
    - Obrázek produktu, jehož velikost lze automaticky změnit tak, aby vyhovovala různým velikostem oblasti zobrazení
    - Alternativní text pro obrázek produktu
    - Jednotková cena produktu

## <a name="abandoned-cart-connector-sample"></a>Ukázka konektoru opuštěného košíku

Model konektoru, který společnost Microsoft poskytuje prostřednictvím sady SDK (Retail software development kit), umožňuje načíst informace o opuštěném košíku a odeslat je poskytovateli e-mailového marketingu třetí strany. Tento konektor zpracovává komunikaci se Serverem maloobchodu, používá trezor Azure Key Vault k zabezpečení košíku, zpracovává plánování načítání košíku v zadaném časovém oknu a načítá data o objednávkách a produktech. Poskytuje také ukázkovou implementaci pro integraci s poskytovatelem e-mailového marketingu třetí strany. Konektor má integrovanou komunikaci se systémem [Emarsys](https://emarsys.com). Lze jej však snadno přizpůsobit a integrovat s jinými řešeními, jako je Constant Contact, Mailchimp a SendGrid.

Následující obrázek ukazuje součásti ukázkové aplikace konektoru opuštěného košíku.

![Komponenty ukázkové aplikace konektoru opuštěného košíku](media/AbandonedCartConnector.png)

> [!IMPORTANT]
> Některé oblasti vyžadují, aby odběratelé mohli výslovně nesouhlasit s předáváním údajů z košíku poskytovateli e-mailového marketingu, nebo požádat o odstranění svých údajů. Společnost Microsoft však tyto možnosti zákazníkům neposkytuje. Pokud tedy plánujete podnikat v oblastech, které toto nařizují, musíte poskytnout požadovanou infrastrukturu a přizpůsobení pro sledování preferencí zákazníků a na jejich základě zabránit předávání zákaznických dat do vaší e-mailové platformy. Musíte také definovat proces pro vymazání zákaznických dat u vašeho poskytovatele e-mailového marketingu na žádost zákazníka.

## <a name="obtain-the-code-sample"></a>Získání ukázkového kódu

Ukázková aplikace konektoru opuštěného košíku je součástí sady Retail SDK od verze 10.0.16. Kód najdete ve složce **\\RetailSDK\\Code\\SampleExtensions\\RetailServer\\Extensions.AbandonedCartSample**. Další informace o instalaci a použití sady Retail SDK a ejím získání naleznete v tématu [Sada Retail software development kit (SDK)](retail-sdk/retail-sdk-overview.md).

> [!NOTE]
> Přestože byl ukázkový kód poprvé zpřístupněn ve verzi 10.0.16, je kompatibilní s verzí 10.0.13 a novějšími sestaveními Serveru maloobchodu.

## <a name="prerequisites-and-dependencies"></a>Předpoklady a závislosti

Než budete moci nasadit a nakonfigurovat ukázkový kód konektoru opuštěného košíku, musí být splněny následující předpoklady.

### <a name="access-to-commerce-resources"></a>Přístup ke zdrojům Commerce

Chcete-li nakonfigurovat a nasadit aplikaci konektoru opuštěného košíku, musíte mít přístup k následujícím zdrojům Commerce:

- Administrátorský přístup do centrály Commerce pro vaše prostředí
- Přístup k projektu sluzeb Microsoft Dynamics Lifecycle Services (LCS) pro vaše prostředí

### <a name="azure-cosmos-db"></a>Azure Cosmos DB

Aplikace konektoru opuštěného košíku používá Azure Cosmos DB ke sledování ID a časových razítek košíků, které byly dříve načteny. K trvalému uchování těchto dat můžete použít databázi Azure Cosmos DB, nebo můžete upravit ukázkový kód tak, aby integroval jinou možnost ukládání dat. Další informace o Azure Cosmos DB najdete v tématu [Vítejte v Azure Cosmos DB](/azure/cosmos-db/introduction).

Pokud používáte Azure Cosmos DB, musejí být splněny následující předpoklady, než budete moci spustit ukázkovou aplikaci:

- Musíte mít aktivní účet Azure Cosmos DB. Pokud nemáte účet, postupujte dle tématu [Vytvoření databázového účtu](/azure/cosmos-db/create-sql-api-dotnet#create-a-database-account).
- Musíte načíst hodnoty **URI** a **PRIMARY KEY** (nebo **SECONDARY KEY**) z listu **Klíče** vašeho účtu Azure Cosmos DB v portálu Azure. Další informace o načtení koncového bodu a informací klíčů z účtu Azure Cosmos DB najdete v tématu [Zobrazení, kopírování a opětovné generování přístupových klíčů a hesel](/azure/cosmos-db/manage-account#keys).

### <a name="azure-key-vault"></a>Azure Key Vault

Aplikace konektoru opuštěného košíku používá Key Vault k ukládání názvů a tajných kódů různých komponent, které vyžadují bezpečný přístup.

Při nastavení trezoru klíčů postupujte následujícím způsobem.

1. Postupujte podle pokynů v tématu [Správa Key Vault v Azure Stack Hub pomocí portálu](/azure-stack/user/azure-stack-key-vault-manage-portal?view=azs-2002&preserve-view=true).
2. Vytvořte tajné kódy pro následující informace:

    - Uživatelské jméno a tajný kód API rozhraní API Emarsys
    - ID a tajný kód aplikace opuštěného košíku

Ukázkový kód konektoru opuštěného košíku používá výchozí přihlašovací údaje Azure pro přístup do Key Vault. Musíte poskytnout oprávnění **Seznam** a **Číst** k identitě, kterou plánujete používat pro přístup do Key Vault.

Další informace o výchozích přihlašovacích údajích Azure najdete v tématu [Třída DefaultAzureCredential](/dotnet/api/azure.identity.defaultazurecredential?view=azure-dotnet&preserve-view=true).

## <a name="create-an-abandoned-cart-connector-sample-app-application-id-for-the-azure-ad-tenant"></a>Vytvoření ID vzorové aplikace konektoru opuštěného košíku pro klienta Azure AD

Musíte vytvořit ID vzorové aplikace konektoru opuštěného košíku pro klienta Azure Active Directory (AD). Informace o vytváření ID aplikace naleznete v části [Použití portálu k vytvoření aplikace Azure AD a hlavní služby, které mají přístup ke zdrojům](/azure/active-directory/develop/howto-create-service-principal-portal).

## <a name="add-the-abandoned-cart-connector-sample-app-application-id-to-the-allow-list-for-the-retail-server-api"></a>Přidání ID vzorové aplikace konektoru opuštěného košíku do seznamu povolených pro rozhraní API Serveru maloobchodu

Dále musíte přidat ID vzorové aplikace konektoru opuštěného košíku do seznamu povolených pro rozhraní API Serveru maloobchodu. Informace o tom, jak přidat ID aplikace do seznamu povolených v Azure, najdete v článku komunity [Support for Service to Service authentication in Retail Server](https://community.dynamics.com/ax/b/axforretail/posts/support-for-service-to-service-authentication-in-retail-server).

## <a name="configure-the-abandoned-cart-connector-sample-app"></a>Konfigurace ukázkové aplikace konektoru opuštěného košíku

Chcete-li nakonfigurovat ukázkovou aplikaci konektoru opuštěného košíku, upravte konfigurační soubor **appSettings.json**, který je umístěn v kořenu adresáře **AbandonedCartDetectionSample**. Následující tabulky popisují vlastnosti konfiguračního souboru.

### <a name="keyvaultoptions"></a>KeyVaultOptions

| Vlastnost    | Popis |
| ----------- | ----------- |
| KeyVaultURI | Název DNS (Domain Name System) trezoru klíčů, který používáte v portálu Azure. |

### <a name="retailserverclientoptions"></a>RetailServerClientOptions

| Vlastnost                                      | Popis |
| --------------------------------------------- | ----------- |
| TenantId                                      | ID klienta Azure AD vašeho tenanta Azure. |
| RetailServerAudienceId                        | ID cílové skupiny Serveru maloobchodu. Výchozí hodnotu můžete ponechat. |
| AppIdKeyVaultSecretName                       | Název tajného kódu, který jste vytvořili pro ID vzorové aplikace konektoru opuštěného košíku. |
| AppSecretKeyVaultSecretName                   | Název tajného kódu, ve kterém je uložen tajný kód vzorové aplikace konektoru opuštěného košíku. |
| RetailServerUrl                               | Adresa URL vaší instance Serveru maloobchodu. Tuto hodnotu najdete v LCS. |
| OperatingUnitNumber                           | Číslo provozní jednotky (OUN). Tuto hodnotu najdete v centrále Commerce. |
| IncludeAbandonedCartsModifiedSinceLastMinutes | Začátek časového okna pro opuštěné košíky, které chcete načíst. Hodnota je vyjádřena jako počet minut před aktuálním časem. Nastavte tuto vlastnost například na **120**, když chcete načíst všechny košíky, které byly naposledy upraveny v období 120 minut před koncem časového okna, které je definováno vlastností **ExcludeAbandonedCartsModifiedSinceLastMinutes**. |
| ExcludeAbandonedCartsModifiedSinceLastMinutes | Konec časového okna pro opuštěné košíky, které chcete načíst. Hodnota je vyjádřena jako počet minut před aktuálním časem. Například když je vlastnost **IncludeAbandonedCartsModifiedSinceLastMinutes** nastavena na **120**, nastavte tuto vlastnost na **30**, když mají být načteny všechny košíky, které byly upraveny v intervalu 120 minut až 30 minut před aktuálním časem. V praxi tato vlastnost definuje dobu, po kterou chcete čekat, než bude košík prohlášen za opuštěný. |
| ReturnToCartUrl                               | Adresa URL košíku na vašem webu elektronického obchodu ve formátu, který se používá v souboru **app.config**. |

### <a name="azurecosmosoptions"></a>AzureCosmosOptions

Stav úlohy načítání opuštěného košíku, ID košíků a upravená časová razítka jsou uloženy v databázi Azure Cosmos DB. Ve výchozím nastavení odkazují nastavení v konfiguračním souboru na instanci místního emulátoru Azure Cosmos DB. Když nasadíte konektor do produkčního prostředí, musíte aktualizovat tato nastavení, aby odkazovala na instanci Azure Cosmos DB ve vašem předplatném Azure. Pro místní testování nebo testování v sandboxu můžete použít [emulátor Azure Cosmos](/azure/cosmos-db/local-emulator).

| Vlastnost    | Popis |
| ----------- | ----------- |
| EndPointUri | Identifikátor URI koncového bodu, který poskytuje Azure nebo emulátor. |
| PrimaryKey  | Primární klíč, který poskytuje Azure nebo emulátor. |
| DatabaseId  | ID databáze. Můžete ponechat výchozí hodnotu nebo zadat vlastní. |
| ContainerId | ID kontejneru. Můžete ponechat výchozí hodnotu nebo zadat vlastní. |

### <a name="emarsysclientoptions"></a>EmarsysClientOptions

> [!NOTE]
> Pokud se integrujete s jiným poskytovatelem e-mailového marketingu než Emarsys, musíte rozšířit rozhraní **IEmailProvider** podle potřeby pro komunikaci s tímto poskytovatelem.

| Vlastnost                      | Popis |
| ----------------------------- | ----------- |
| ApiUrl                        | `https://api.emarsys.net/api/v2/event/{0}/trigger` |
| ExternalEventId               | ID externího záznamu události, který je vytvořen v Emarsys. Hodnotu najdete v části **Nastavení triggeru** v kampani, kterou jste vytvořili za účelem zasílání e-mailových upozornění na opuštěný košík. |
| ApiUserNameKeyVaultSecretName | Název klíče, ve kterém je uloženo uživatelské jméno Emarsys API. |
| ApiSecretKeyVaultSecretName   | Název klíče, ve kterém je uložen tajný kód Emarsys API. |
| EmarsysContactKeyId           | ID sloupce e-mailu v databázi kontaktů Emarsys. Výchozí hodnota je **3** a neměla by se měnit. |

### <a name="mediaoptions"></a>MediaOptions

Pokud používáte funkce elektronického obchodování v Commerce, můžete k načtení obrázků produktů použít správu digitálních informací Commerce. Další informace o možnostech změny velikosti obrázků ve správě digitálních informací naleznete v části [Konfigurace oblasti zobrazení ImageSettings](../e-commerce-extensibility/image-component.md#imagesettings-viewport-configuration).

| Vlastnost                             | Popis |
| ------------------------------------ | ----------- |
| ImageServerUrl                       | Kořenová adresa URL správce digitálních informací vašeho webu. Hodnotu najdete v klíči vlastnosti **Základní adresa URL mediálního serveru** v nabídce **Maloobchodní a velkoobchodní prodej \> Nastavení kanálu \> Profily kanálů** v centrále Commerce. |
| ImageViewPorts                       | Uzel kontejneru pro jednotlivé konfigurace oblasti zobrazení. |
| ImageViewPorts/viewport              | Definice oblasti zobrazení. Tuto vlastnost použijte k určení rozsahů šířky oblasti zobrazení v pixelech. Příklad, který ukazuje, jak se tato vlastnost používá, najdete v konfiguračním souboru **appSettings.json**. |
| ImageViewPorts/imageWidth            | Šířka obrazu v oblasti zobrazení v pixelech. |
| imageViewPorts/imageHeight           | Výška obrazu v oblasti zobrazení v pixelech. |
| imageViewPorts/useForDefaultImageTag | Hodnota **true**/**false**, která udává, zda mají být použity rozměry obrázku, které jsou definovány oblastí zobrazení, pokud značka `<picture>` jazyka HTML není ve webovém prohlížeči nebo e-mailovém klientu podporována. |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
