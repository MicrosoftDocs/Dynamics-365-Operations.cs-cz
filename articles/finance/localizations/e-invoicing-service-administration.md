---
title: Komponenty pro správu doplňku elektronického fakturování
description: Toto téma poskytuje informace o komponentách, které souvisejí se správou doplňku elektronické fakturace.
author: gionoder
manager: AnnBe
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: 6f630ebb694217c3bd52378a649933a670c090f2
ms.sourcegitcommit: e88c96d1cb817a22db81856cadb563c095ab2671
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/02/2021
ms.locfileid: "5104355"
---
# <a name="electronic-invoicing-add-on-administration-components"></a>Komponenty pro správu doplňku elektronického fakturování

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Toto téma poskytuje informace o komponentách, které souvisejí se správou doplňku elektronické fakturace. Poskytuje také informace, jak konfigurovat službu doplňku elektronické fakturace.

## <a name="azure"></a>Azure

Použijte Microsoft Azure k vytvoření tajných klíčů pro trezor klíčů a účet úložiště. Potom použijte tajné klíče v konfiguraci doplňku elektronické fakturace.

## <a name="lifecycle-services"></a>Lifecycle Services

Pomocí Microsoft Dynamics Lifecycle Services (LCS) povolte doplněk pro mikroslužby pro váš projekt nasazení LCS.

V LCS vyberte dlaždici **Správa funkcí Preview** a poté zapněte funkci **Služba elektronické fakturace**.

## <a name="regulatory-configuration-services"></a>Regulatory Configuration Services

Dynamics 365 Regulatory Configuration Services (RCS) je rozhraní, které se používá ke konfiguraci doplňku elektronické fakturace. Prostředky typu prostředí nebo funkce elektronické fakturace jsou vytvářeny, udržovány a hostovány v RCS. Když jsou prostředky připraveny, jsou publikovány ve službě doplňku elektronické fakturace.

Pro více informací o RCS viz [Regulatory Configuration Services (RCS) – funkce globalizace](rcs-globalization-feature.md)

### <a name="integration-with-the-electronic-invoicing-add-on"></a>Integrace s doplňkem elektronické fakturace

Než budete pomocí RCS moci konfigurovat elektronické faktury, musíte nakonfigurovat RCS tak, aby umožňovalo komunikaci s doplňkem elektronické fakturace. Tuto konfiguraci provedete na kartě **Doplněk elektronické fakturace** na stránce **Parametry elektronického vykazování**.

#### <a name="service-endpoint"></a>Koncový bod služby

Adresa URL koncového bodu doplňku elektronické fakturace se může lišit podle geografie datového centra Azure. Následující tabulka uvádí dostupnost podle oblastí:

| Geografie datového centra Azure | URL adresa koncového bodu služby                                                       |
|----------------------------|----------------------------------------------------------------------------|
| Východní USA                    | `https://electronicinvoicing.eus-il301.gateway.prod.island.powerapps.com/` |
| USA – západ                    | `https://electronicinvoicing.wus-il301.gateway.prod.island.powerapps.com/` |
| Sever EU                   | `https://electronicinvoicing.neu-il301.gateway.prod.island.powerapps.com/` |
| Západ EU                    | `https://electronicinvoicing.weu-il301.gateway.prod.island.powerapps.com/` |

#### <a name="application-id"></a>ID přihlášky

ID aplikace je ID aplikace doplňku elektronické fakturace. V tomto případě je hodnota pevná: **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.

#### <a name="lcs-environment-id"></a>ID prostředí LCS

ID prostředí LCS je ID předplatného LCS vaší organizace.

### <a name="service-environments"></a>Prostředí služby

Prostředí služeb jsou logické oddíly, které jsou vytvořeny na podporu provádění funkcí elektronické fakturace v doplňku elektronické fakturace. Tajné klíče zabezpečení a digitální certifikáty a správa (tj. přístupová oprávnění) musí být nakonfigurovány na úrovni prostředí služby.

Zákazníci mohou vytvořit tolik prostředí služeb, kolik chtějí. Všechna prostředí služeb, která zákazník vytvoří, jsou na sobě navzájem nezávislá.

Prostředí služeb musí být vytvořena a udržována v RCS. Když jsou prostředí služeb připraveny, musí být publikovány v doplňku elektronické fakturace.

#### <a name="service-environment-status"></a>Stav prostředí služeb

Prostředí služeb lze spravovat prostřednictvím stavu. K dispozici jsou tyto možnosti:

- **Nepublikováno** – Prostředí bylo vytvořeno, ale dosud nebylo publikováno.
- **Publikováno** – Prostředí bylo publikováno v doplňku elektronické fakturace.
- **Změněno** – Atributy publikovaného prostředí byly změněny, ale změny ještě nebyly publikovány.

#### <a name="customer-secrets"></a>Tajné klíče zákazníků

Doplňková služba elektronické fakturace je zodpovědná za ukládání všech vašich obchodních údajů v prostředcích Azure, které vlastní vaše společnost. Abyste zajistili, že služba funguje správně a že ke všem obchodním datům, která jsou potřebná a generovaná doplňkem elektronické fakturace, přistupuje pouze doplněk, musíte vytvořit dva hlavní prostředky Azure:

- Účet úložiště Azure (úložiště Blob), které bude uchovávat elektronické faktury
- Trezor klíčů Azure, který bude uchovávat certifikáty a identifikátor URI (Uniform Resource Identifier) účtu úložiště

> [!NOTE]
> Vyhrazený trezor klíčů a účet úložiště odběratele musí být výslovně přiděleny pro použití s doplňkem elektronické fakturace.

Další informace viz [Vytvoření účtu úložiště a trezoru klíčů Azure](e-invoicing-create-azure-storage-account-key-vault.md).

#### <a name="users"></a>Uživatelé

Každé prostředí služeb musí obsahovat seznam uživatelů, kteří se mohou připojit z aplikací Dynamics 365 Finance a Dynamics 365 Supply Chain Management v doplňku elektronické fakturace.

#### <a name="publication"></a>Publikování

Prostředí služeb musí být publikovány v doplňku elektronické fakturace, než je možné je použít. Aplikace Finance a Supply Chain Management mají přístup pouze k publikovaným prostředím. Kromě toho musí být prostředí služeb publikováno, než se jakékoli aktualizace jeho atributů projeví ve službě elektronické fakturace.

### <a name="connected-applications"></a>Připojené aplikace

Připojené aplikace jsou instance aplikací Finance a Supply Chain Management, ke kterým byste se mohli chtít připojit prostřednictvím RCS. Kromě adresy URL aplikace a jejího klienta obsahuje připojená aplikace pověření, která umožňují RCS připojit se k prostředí.

Prostřednictvím připojených aplikací můžete nakonfigurovat část funkce elektronické fakturace v aplikacích Finance a Supply Chain Management, aby byla funkční celá funkce elektronické fakturace.

## <a name="finance-and-supply-chain-management"></a>Finance a Supply Chain Management

### <a name="integration-with-electronic-invoicing-add-on"></a>Integrace s doplňkem elektronické fakturace

Než budete moci použít aplikace Finance a Supply Chain Management k vystavování elektronických faktur pomocí doplňku elektronické fakturace, musí být doplněk nakonfigurován tak, aby umožňoval komunikaci se službou.

#### <a name="electronic-invoicing-add-on-integration-feature"></a>Funkce integrace doplňku elektronické fakturace

Aby bylo možné povolit komunikaci mezi aplikacemi Finance a Supply Chain Management a doplňkem elektronické fakturace, musíte zapnout funkci **Integrace doplňku elektronické fakturace** v pracovním prostoru **Správa funkcí**.

#### <a name="service-endpoint"></a>Koncový bod služby

Koncovým bodem služby je adresa URL, kde se nachází doplněk elektronické fakturace. Než budete moci vystavovat elektronické faktury, v aplikacích Finance a Supply Chain Management musí být nakonfigurován koncový bod služby, aby byla možná komunikace se službou.

Chcete-li nakonfigurovat koncový bod služby, přejděte na **Správa organizace \> Nastavení \> Parametr elektronického dokumentu** a poté na kartě **Služby odesílání** v poli **Adresa URL doplňku elektronické fakturace** zadejte adresu URL, jak je popsáno v tabulce v části **Koncový bod služby**.

#### <a name="environments"></a>Prostředí

Název prostředí zadaný v aplikacích Finance and Supply Chain Management odkazuje na název prostředí vytvořeného v RCS a publikovaného v doplňku elektronické fakturace.

Prostředí musí být nakonfigurováno na kartě **Služby odesílání** na stránce **Parametr elektronického dokumentu**, aby každý požadavek na vystavení elektronické faktury obsahoval prostředí, podle kterého může doplněk elektronické fakturace určit, která funkce elektronické fakturace má požadavek zpracovat.

## <a name="additional-resources"></a>Další prostředky

- [Konfigurace elektronických faktur v RCS](e-invoicing-configuration-rcs.md)
- [Vystavení elektronických faktur v aplikacích Finance a Supply Chain Management](e-invoicing-issuing-electronic-invoices-finance-supply-chain-management.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]