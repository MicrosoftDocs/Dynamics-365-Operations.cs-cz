---
title: Chyba certifikační cesty při nastavování připojení aplikace
description: Pokud aplikace Warehouse Management zobrazuje chybu „Důvěryhodná kotva pro certifikační cestu nebyla nalezena“, použijte tuto stránku k řešení nebo vyřešení problému.
author: ivanv-microsoft
ms.date: 06/24/2021
ms.topic: troubleshooting
ms.search.form: WMA
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ivanv
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: e4a36874ac4982c9c92a7dcc17c13c7c7c02bf8c
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475799"
---
# <a name="trust-anchor-for-certification-path-not-found-when-setting-up-app-connection"></a>Při nastavování připojení aplikace nebyla nalezena důvěryhodná kotva pro certifikační cestu

## <a name="symptoms"></a>Příznaky

Při pokusu o připojení k Supply Chain Management vám aplikace Warehouse Management může zobrazit následující chybovou zprávu:

> Nebyla nalezena důvěryhodná kotva pro certifikační cestu.

Tento problém může ovlivnit zařízení s následujícími vlastnostmi:

- **Verze OS**: Android 4.4.x (například Zebra TC55). V poslední době to není problém verzí Android.
- **Umístění Supply Chain Management**: Cloud
- **Režim připojení**: Tajný klíč nebo certifikát klienta

## <a name="possible-cause"></a>Možná příčina

Společnost Microsoft pravděpodobně aktualizovala certifikáty SSL serveru používané v Supply Chain Management. V důsledku toho se mohl změnit kořenový certifikát a/nebo jeden z přechodných certifikátů, takže nový certifikát není na seznamu důvěryhodných systémových certifikátů pro mobilní zařízení. Novější verze systému Android automaticky aktualizují seznamy důvěryhodných certifikátů, ale Android 4.4.x ne.

## <a name="resolution"></a>Řešení

K vyřešení problému proveďte některý z následujících kroků:

- Pomocí řešení popsaného v následující části aktualizujte všechna relevantní zařízení.
- *Mohlo* by být možné kontaktovat společnost Zebra nebo Google a získat aktualizaci certifikátů systému důvěryhodné certifikační autority (CA). To jsme však nepotvrdili.
- Pokud je to možné, zvažte nahrazení starších zařízení zařízeními, která používají novější verzi systému Android (kde se důvěryhodné certifikáty CA aktualizují automaticky).

### <a name="workaround"></a>Alternativní řešení

#### <a name="step-1-export-the-new-root-certificate-from-supply-chain-management"></a>Krok 1: Exportujte nový kořenový certifikát ze Supply Chain Management

Ručně stáhněte nový kořenový certifikát pomocí internetového prohlížeče následujícím způsobem:

1. Přihlaste se do Dynamics Supply Chain Management a otevřete úvodní stránku.

1. V adresním řádku prohlížeče vyberte ikonu zámku a otevřete dialogové okno **Poloha je zabezpečená**.
1. V dialogovém okně vyberte **Certifikát (platný)** k otevření okna **Certifikát** pro tento certifikát.
1. Otevřete kartu **Cesta k certifikátu** v okně **Certifikát**.
1. Vyberte nejvyšší certifikát zobrazený v hierarchii. (toto je kořenový certifikát).
1. Otevřete kartu **Podrobnosti** v okně **Certifikát**.
1. Vyberte tlačítko **Kopírovat do souboru** ve spodní části karty **Podrobnosti**.
1. Otevře se **Průvodce exportem certifikátu**. Pokračujte výběrem tlačítka **Další**.
1. Otevře se stránka **Exportovat formát souboru**. Vyberte **Binární X.509 s kódováním DER (.CER)**. Pak pokračujte výběrem tlačítka **Další**.
1. Otevře se stránka **Soubory k exportu**, zadejte název souboru a umístění. Pak pokračujte výběrem tlačítka **Další**.
1. Otevře se stránka **Dokončení průvodce exportem certifikátu** zobrazující výsledek vašeho exportu. Vyberte **Dokončit**.

#### <a name="step-2-install-the-downloaded-certificate-onto-the-affected-devices"></a>Krok 2: Nainstalujte stažený certifikát na příslušná zařízení

Nainstalujte stažený certifikát následujícím způsobem:

1. Přeneste certifikát, který jste stáhli v předchozím kroku, do zařízení, které chcete aktualizovat. Můžete například použít kartu SD nebo síťové připojení, abyste soubor zpřístupnili svému zařízení.
1. Otevřete nastavení zabezpečení pro své zařízení a vyberte možnost nabídky pro instalaci certifikátu ze souboru. (Přesné kroky se liší podle verze zařízení a operačního systému.)
1. Nový certifikát by nyní měl být zobrazen na kartě **Uživatel** pro důvěryhodné certifikáty.
1. Tento postup opakujte pro každé ovlivněné zařízení.
