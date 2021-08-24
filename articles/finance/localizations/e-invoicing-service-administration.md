---
title: Součásti pro správu Elektronické fakturace
description: Toto téma poskytuje informace o součástech, které souvisejí se správou Elektronické fakturace.
author: gionoder
ms.date: 04/29/2021
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
ms.openlocfilehash: 6582a0a9eda19fe69ead853ea5d79d763afcb8a468717fde84a32146fd0f79af
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6721719"
---
# <a name="electronic-invoicing-administration-components"></a>Součásti pro správu Elektronické fakturace

[!include [banner](../includes/banner.md)]


Toto téma poskytuje informace o součástech, které souvisejí se správou Elektronické fakturace. Obsahuje také informace o konfiguraci služby elektronické fakturace.

## <a name="azure"></a>Azure

Použijte Microsoft Azure k vytvoření tajných klíčů pro trezor klíčů a účet úložiště. Potom použijte tajné klíče v konfiguraci Elektronické fakturace.

## <a name="lifecycle-services"></a>Lifecycle Services

Pomocí Microsoft Dynamics Lifecycle Services (LCS) povolte mikroslužby pro váš projekt nasazení LCS.

> [!NOTE]
> Instalace mikroslužeb v LCS vyžaduje alespoň virtuální počítač úrovně 2. Další informace o plánování prostředí naleznete v části [Plánování prostředí](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).
 

## <a name="regulatory-configuration-services"></a>Regulatory Configuration Services

Dynamics 365 Regulatory Configuration Services (RCS) je rozhraní, které se používá ke konfiguraci Elektronické fakturace. Prostředky typu prostředí nebo funkce elektronické fakturace jsou vytvářeny, udržovány a hostovány v RCS. Když jsou prostředky připraveny, jsou publikovány ve službě elektronické fakturace.

Registrace RCS viz [Regulatory services](https://marketing.configure.global.dynamics.com/).

Pro více informací o RCS viz [Regulatory Configuration Services (RCS) – funkce globalizace](rcs-globalization-feature.md)

### <a name="integration-with-electronic-invoicing"></a>Integrace s Elektronickou fakturací 

Než budete pomocí RCS moci konfigurovat elektronické faktury, musíte nakonfigurovat RCS tak, aby umožňovalo komunikaci s Elektronickou fakturací. Tuto konfiguraci provedete na kartě **Elektronická fakturace** na stránce **Parametry elektronického vykazování**.

#### <a name="service-endpoint"></a>Koncový bod služby

Elektronická fakturace je k dispozici v několika geografických oblastech datového centra Azure. Následující tabulka uvádí dostupnost podle oblastí.

| Geografie datového centra Azure |
|----------------------------|
| Spojené státy americké              |
| Evropa                     |
| Spojené království             |
| Asie                       |

### <a name="service-environments"></a>Prostředí služby

Prostředí služeb jsou logické oddíly, které jsou vytvořeny na podporu provádění funkcí elektronické fakturace v Elektronické fakturaci. Tajné klíče zabezpečení a digitální certifikáty a správa (tj. přístupová oprávnění) musí být nakonfigurovány na úrovni prostředí služby.

Zákazníci mohou vytvořit tolik prostředí služeb, kolik chtějí. Všechna prostředí služeb, která zákazník vytvoří, jsou na sobě navzájem nezávislá.

Prostředí služeb musí být vytvořena a udržována v RCS. Když jsou prostředí služeb připraveny, musí být publikovány v Elektronické fakturaci.

#### <a name="service-environment-status"></a>Stav prostředí služeb

Prostředí služeb lze spravovat prostřednictvím stavu. K dispozici jsou tyto možnosti:

- **Nepublikováno** – Prostředí bylo vytvořeno, ale dosud nebylo publikováno.
- **Publikováno** – Prostředí bylo publikováno v Elektronické fakturaci.
- **Změněno** – Atributy publikovaného prostředí byly změněny, ale změny ještě nebyly publikovány.

#### <a name="customer-secrets"></a>Tajné klíče zákazníků

Služba elektronické fakturace je zodpovědná za ukládání všech vašich obchodních údajů v prostředcích Azure, které vlastní vaše společnost. Abyste zajistili, že služba funguje správně a že ke všem obchodním datům, která jsou potřebná a generovaná Elektronickou fakturací, se přistupuje správným způsobem, musíte vytvořit dva hlavní zdroje Azure:

- Účet úložiště Azure (úložiště Blob), které bude uchovávat elektronické faktury
- Trezor klíčů Azure, který bude uchovávat certifikáty a identifikátor URI (Uniform Resource Identifier) účtu úložiště


Vyhrazený trezor klíčů a účet úložiště odběratele musí být výslovně přiděleny pro použití s Elektronickou fakturací. Další informace viz [Vytvoření účtu úložiště a trezoru klíčů Azure](e-invoicing-create-azure-storage-account-key-vault.md).

Chcete-li sledovat stav vašeho trezoru klíčů a přijímat upozornění, nakonfigurujte Azure Monitor pro trezor klíčů. Povolením protokolování trezoru klíčů můžete sledovat, jak, kdy a kým je k vašim trezorům klíčů přistupováno. Další informace viz [Monitorování a varování pro Azure Key Vault](/azure/key-vault/general/alert) a [Jak povolit protokolování trezoru klíčů](/azure/key-vault/general/howto-logging?tabs=azure-cli).

Osvědčeným postupem je pravidelně střídat tajné klíče. Další informace naleznete v [Dokumentace k tajným klíčům](/azure/key-vault/secrets/).

#### <a name="users"></a>Uživatelé

Každé prostředí služeb musí obsahovat seznam uživatelů, kteří se mohou připojit z aplikací Dynamics 365 Finance a Dynamics 365 Supply Chain Management v Elektronické fakturaci.

#### <a name="publication"></a>Publikování

Prostředí služeb musí být publikovány v Elektronické fakturaci, než je možné je použít. Aplikace Finance a Supply Chain Management mají přístup pouze k publikovaným prostředím. Kromě toho musí být prostředí služeb publikováno, než se jakékoli aktualizace jeho atributů projeví ve službě elektronické fakturace.

### <a name="connected-applications"></a>Připojené aplikace

Připojené aplikace jsou instance aplikací Finance a Supply Chain Management, ke kterým byste se mohli chtít připojit prostřednictvím RCS. Kromě adresy URL aplikace a jejího klienta obsahuje připojená aplikace pověření, která umožňují RCS připojit se k prostředí.

Prostřednictvím připojených aplikací můžete nakonfigurovat část funkce elektronické fakturace v aplikacích Finance a Supply Chain Management, aby byla funkční celá funkce elektronické fakturace.

## <a name="finance-and-supply-chain-management"></a>Finance a Supply Chain Management

### <a name="integration-with-electronic-invoicing"></a>Integrace s Elektronickou fakturací

Než budete moci použít aplikace Finance a Supply Chain Management k vystavování elektronických faktur pomocí Elektronické fakturace, musí být tato aplikace konfigurována tak, aby umožňovala komunikaci se službou.

#### <a name="electronic-invoicing-integration-feature"></a>Funkce integrace Elektronické fakturace

Aby bylo možné povolit komunikaci mezi aplikacemi Finance a Supply Chain Management a Elektronickou fakturací, musíte zapnout funkci možnost **Integrace elektronické fakturace** v pracovním prostoru **Správa funkcí**.

#### <a name="service-endpoint"></a>Koncový bod služby

Koncovým bodem služby je adresa URL, kde se nachází Elektronická fakturace. Než budete moci vystavovat elektronické faktury, v aplikacích Finance a Supply Chain Management musí být nakonfigurován koncový bod služby, aby byla možná komunikace se službou.

Chcete-li nakonfigurovat koncový bod služby, přejděte na **Správa organizace \> Nastavení \> Parametr elektronického dokumentu** a poté na kartě **Služby odesílání** v poli **Adresa URL elektronické fakturace** zadejte adresu URL, jak je popsáno v tabulce v části **Koncový bod služby**.

#### <a name="environments"></a>Prostředí

Název prostředí zadaný v aplikacích Finance a Supply Chain Management odkazuje na název prostředí vytvořeného v RCS a publikovaného v Elektronické fakturaci.

Prostředí musí být nakonfigurováno na kartě **Služby odesílání** na stránce **Parametr elektronického dokumentu**, aby každý požadavek na vystavení elektronické faktury obsahoval prostředí, podle kterého může Elektronická fakturace určit, která funkce elektronické fakturace má požadavek zpracovat.

## <a name="additional-resources"></a>Další prostředky

- [Konfigurace elektronických faktur v RCS](e-invoicing-configuration-rcs.md)
- [Vystavení elektronických faktur v aplikacích Finance a Supply Chain Management](e-invoicing-issuing-electronic-invoices-finance-supply-chain-management.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
