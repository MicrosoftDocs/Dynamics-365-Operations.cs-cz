---
title: Začínáme s Elektronickou fakturací
description: Toto téma poskytuje informace, které vám pomohou začít s Elektronickou fakturací v Microsoft Dynamics 365 Finance a Dynamics 365 Supply Chain Management.
author: gionoder
ms.date: 08/17/2021
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
ms.openlocfilehash: d0550228dc77ed255a0033bc3b0a4ec21d48a497
ms.sourcegitcommit: 2113678369f47944f8725ca656f461fa159f87f6
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/27/2021
ms.locfileid: "7700372"
---
# <a name="get-started-with-electronic-invoicing"></a>Začínáme s Elektronickou fakturací

[!include [banner](../includes/banner.md)]

Toto téma poskytuje informace, které vám pomohou začít s Elektronickou fakturací. Toto téma vás provede běžnými kroky konfigurace služeb Regulatory Configuration Services (RCS) a Dynamics 365 Finance, a popisuje kroky, které musíte dodržet při odesílání obchodních dokumentů a kontrole výsledků zpracování.

## <a name="prerequisites"></a>Předpoklady

Než provedete postupy v tomto tématu, musí být splněny následující předpoklady:

- Nakonfigurujte služby Microsoft Dynamics Lifecycle Services (LCS), Regulatory Configuration Service (RCS) a prostředí Microsoft Dynamics 365 Finance nebo Dynamics 365 Supply Chain Management. Další informace najdete v tématu [Začínáme se správou služby Elektronické fakturace](e-invoicing-get-started-service-administration.md).
- Vytvořte poskytovatele konfigurace pro vaši organizaci. Další informace naleznete v tématu [Vytvoření poskytovatelů konfigurace a jejich označení jako aktivních](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).

## <a name="import-an-electronic-invoicing-feature-from-the-microsoft-configuration-provider"></a>Importujte funkci elektronické fakturace od poskytovatele konfigurace společnosti Microsoft 

1. Přihlaste se ke svému účtu Regulatory Configuration Service (RCS).
2. V pracovním prostoru **Funkce globalizace** v části **Funkce** vyberte dlaždici **Elektronická fakturace**.
3. Vyberte **Import** a potom vyberte **Synchronizovat**.
4. Filtrujte sloupec **Poskytovatel konfigurace** sloupec podle výrazu **Microsoft**.
5. V tabulce vyberte název funkce elektronické fakturace a poté vyberte **Import**.

## <a name="create-an-electronic-invoicing-feature-under-your-organization-provider"></a>Vytvoření funkce elektronické fakturace u poskytovatele organizace

1. V RCS v části **Funkce** pracovního prostoru **Funkce globalizace** vyberte dlaždici **Elektronická fakturace**.
2. Vyberte **Přidat** > **Na základě stávající funkce** a do pole **Název** zadejte název funkce elektronické fakturace.
3. Do pole **Popis** zadejte popis funkce.
4. V **poli základní funkce** vyberte importovanou funkci elektronické fakturace od poskytovatele konfigurace společnosti Microsoft.
5. Vyberte **Vytvořit funkci**.

## <a name="country-specific-configuration-for-electronic-invoicing-feature"></a>Konfigurace funkce elektronické fakturace specifická pro zemi

V závislosti na zemi nebo regionu může funkce elektronické fakturace vyžadovat specifickou konfiguraci. 

Konkrétní kroky najdete v dokumentaci „Začínáme“, která je k dispozici pro vaši zemi nebo region.

## <a name="import-the-model-mapping-configurations-from-electronic-reporting"></a>Import konfigurací mapování modelu z elektronického výkaznictví

1. V RCS vyberte pracovní prostor **Elektronické výkaznictví**.
2. V seznamu dostupných poskytovatelů konfigurace **Microsoft** vyberete **Úložiště**.
3. Vyberte **Globální** a v podokně akcí vyberte **Otevřít**.
4. Importujte konfigurace mapování modelu podle následující tabulky na základě názvu prvku.

| Název funkce                         | Konfigurace mapování modelu |
|--------------------------------------|-----------------------------|
| Rakouské elektronické faktury (AT)    | <p>Model kontextu faktury odběratele</p><p>Model faktury</p> |
| Belgická elektronická faktura (BE)      | <p>Model kontextu faktury odběratele</p><p>Model faktury</p> |
| Brazilský NF-e (BR)                  | <p>Model kontextu faktury odběratele</p><p>Fiskální dokumenty</p><p>Model zprávy odpovědi</p> |
| Brazilian NFS-e ABRASF Curitiba (BR) | <p>Model kontextu faktury odběratele</p><p>Fiskální dokumenty</p><p>Model zprávy odpovědi</p> |
| Dánská elektronická faktura (DK)       | <p>Model kontextu faktury odběratele</p><p>Model faktury</p> |
| Egyptská elektronická faktura (EG)     | <p>Model kontextu faktury odběratele</p><p>Model faktury</p><p>Model zprávy odpovědi</p> |
| Estonská elektronická faktura (EE)     | <p>Model kontextu faktury odběratele</p><p>Model faktury</p> |
| Finská elektronická faktura (FI)       | <p>Model kontextu faktury odběratele</p><p>Model faktury</p> |
| Francouzská elektronická faktura (FR)       | <p>Model kontextu faktury odběratele</p><p>Model faktury</p> |
| Německá elektronická faktura (DE)       | <p>Model kontextu faktury odběratele</p><p>Model faktury</p> |
| FatturaPA (IT)                       | <p>Model kontextu faktury odběratele</p><p>Model faktury</p> |
| Mexická CFDI Interfactura (MX)       | <p>Model kontextu faktury odběratele</p><p>Model faktury</p><p>Model zprávy odpovědi</p> |
| Nizozemská elektronická faktura (NL)        | <p>Model kontextu faktury odběratele</p><p>Model faktury</p> |
| Norská elektronická faktura (NO)    | <p>Model kontextu faktury odběratele</p><p>Model faktury</p> |
| Španělská elektronická faktura (ES)      | <p>Model kontextu faktury odběratele</p><p>Model faktury</p> |
| Elektronická faktura PEPPOL            | <p>Model kontextu faktury odběratele</p><p>Model faktury</p> |
| Saúdskoarabská elektronická faktura (SA)| <p>Model kontextu faktury odběratele</p><p>Model faktury</p> |


## <a name="configure-the-application-setup"></a>Konfigurace nastavení aplikace

1. Vyberte funkci elektronické fakturace, kterou jste vytvořili.
2. Na kartě **Nastavení** vyberte **Nastavení aplikace**.
3. V poli **Připojit aplikaci** vyberte připojení, které je spojeno s vaší instancí Finance nebo Supply Chain Management.
4. V části **Typy elektronického dokumentu** vyberte **Přidat**.
5. Vyberte a zadejte **Název tabulky** podle následující tabulky.

    | Název funkce                         | Obchodní dokument | Název tabulky |
    |--------------------------------------|-------------------|------------|
    | Rakouské elektronické faktury (AT)    | <p>Prodejní faktura</p><p>Faktura projektu</p> | <p>Deník faktur odběratele</p><p>Faktura projektu</p> |
    | Belgická elektronická faktura (BE)      | <p>Prodejní faktura</p><p>Faktura projektu</p> | <p>Deník faktur odběratele</p><p>Faktura projektu</p> |
    | Brazilský NF-e (BR)                  | <p>Daňový doklad</p><p>Dopis o opravě</p> | Daňový doklad |
    | Brazilian NFS-e ABRASF Curitiba (BR) | Fiskální dokument služby | Daňový doklad |
    | Dánská elektronická faktura (DK)       | <p>Prodejní faktura</p><p>Faktura projektu</p> | <p>Deník faktur odběratele</p><p>Faktura projektu</p> |
    | Egyptská elektronická faktura (EG)     | <p>Prodejní faktura</p><p>Faktura projektu</p> | <p>Deník faktur odběratele</p><p>Faktura projektu</p> |
    | Estonská elektronická faktura (EE)     | <p>Prodejní faktura</p><p>Faktura projektu</p> | <p>Deník faktur odběratele</p><p>Faktura projektu</p> |
    | Finská elektronická faktura (FI)       | <p>Prodejní faktura</p><p>Faktura projektu</p> | <p>Deník faktur odběratele</p><p>Faktura projektu</p> |
    | Francouzská elektronická faktura (FR)       | <p>Prodejní faktura</p><p>Faktura projektu</p> | <p>Deník faktur odběratele</p><p>Faktura projektu</p> |
    | Německá elektronická faktura (DE)       | <p>Prodejní faktura</p><p>Faktura projektu</p> | <p>Deník faktur odběratele</p><p>Faktura projektu</p> |
    | FatturaPA (IT)                       | <p>Prodejní faktura</p><p>Faktura projektu | <p>Deník faktur odběratele</p><p>Faktura projektu</p> |
    | Mexická CFDI Interfactura (MX)       | <p>Prodejní faktura</p><p>Dodací list</p><p>Převod zásob</p><p>Doplněk platby</p> | Deník faktur odběratele |
    | Nizozemská elektronická faktura (NL)        | <p>Prodejní faktura</p><p>Faktura projektu</p> | <p>Deník faktur odběratele</p><p>Faktura projektu</p> |
    | Norská elektronická faktura (NO)    | <p>Prodejní faktura</p><p>Faktura projektu</p> | <p>Deník faktur odběratele</p><p>Faktura projektu</p> |
    | Španělská elektronická faktura (ES)      | <p>Prodejní faktura</p><p>Faktura projektu</p> | <p>Deník faktur odběratele</p><p>Faktura projektu</p> |
    | Elektronická faktura PEPPOL            | <p>Prodejní faktura</p><p>Faktura projektu</p> | <p>Deník faktur odběratele</p><p>Faktura projektu</p> |
    | Saúdskoarabská elektronická faktura (SA)| <p>Prodejní faktura</p><p>Faktura projektu</p> | <p>Deník faktur odběratele</p><p>Faktura projektu</p> |

6. U každého vytvořeného názvu tabulky vyberte a zadejte kontext podle následující tabulky.

    | Název funkce                         | Obchodní dokument | Kontext |
    |--------------------------------------|-------------------|---------|
    | Rakouské elektronické faktury (AT)    | <p>Prodejní faktura</p><p>Faktura projektu</p> | <p>Kontextový model faktury zákazníka – kontext faktury zákazníka</p><p>Kontextový model faktury zákazníka – kontext faktury projektu</p> |
    | Belgická elektronická faktura (BE)      | <p>Prodejní faktura</p><p>Faktura projektu</p> | <p>Kontextový model faktury zákazníka – kontext faktury zákazníka</p><p>Kontextový model faktury zákazníka – kontext faktury projektu</p> |
    | Brazilský NF-e (BR)                  | <p>Daňový doklad</p><p>Dopis o opravě</p> | <p>Kontextový model faktury zákazníka – kontext fiskálního dokumentu</p><p>Kontextový model faktury zákazníka – kontext dopisu opravy FD</p> |
    | Brazilian NFS-e ABRASF Curitiba (BR) | Fiskální dokument služby| Kontextový model faktury zákazníka – kontext fiskálního dokumentu |
    | Dánská elektronická faktura (DK)       | <p>Prodejní faktura</p><p>Faktura projektu</p> | <p>Kontextový model faktury zákazníka – kontext faktury zákazníka</p><p>Kontextový model faktury zákazníka – kontext faktury projektu</p> |
    | Egyptská elektronická faktura (EG)     | <p>Prodejní faktura</p><p>Faktura projektu</p> | <p>Kontextový model faktury zákazníka – kontext faktury zákazníka</p><p>Kontextový model faktury zákazníka – kontext faktury projektu</p> |
    | Estonská elektronická faktura (EE)     | <p>Prodejní faktura</p><p>Faktura projektu</p> | <p>Kontextový model faktury zákazníka – kontext faktury zákazníka</p><p>Kontextový model faktury zákazníka – kontext faktury projektu</p> |
    | Finská elektronická faktura (FI)       | <p>Prodejní faktura</p><p>Faktura projektu</p> | <p>Kontextový model faktury zákazníka – kontext faktury zákazníka</p><p>Kontextový model faktury zákazníka – kontext faktury projektu</p> |
    | Francouzská elektronická faktura (FR)       | <p>Prodejní faktura</p><p>Faktura projektu</p> | <p>Kontextový model faktury zákazníka – kontext faktury zákazníka</p><p>Kontextový model faktury zákazníka – kontext faktury projektu</p> |
    | Německá elektronická faktura (DE)       | <p>Prodejní faktura</p><p>Faktura projektu</p> | <p>Kontextový model faktury zákazníka – kontext faktury zákazníka</p><p>Kontextový model faktury zákazníka – kontext faktury projektu</p> |
    | FatturaPA (IT)                       | <p>Prodejní faktura</p><p>Faktura projektu</p> | <p>Kontextový model faktury zákazníka – kontext faktury zákazníka</p><p>Kontextový model faktury zákazníka – kontext faktury projektu</p> |
    | Mexická CFDI Interfactura (MX)       | <p>Prodejní faktura</p><p>Dodací list</p><p>Převod zásob</p><p>Doplněk platby</p> | Kontextový model faktury zákazníka – kontext faktury zákazníka |
    | Nizozemská elektronická faktura (NL)        | <p>Prodejní faktura</p><p>Faktura projektu</p> | <p>Kontextový model faktury zákazníka – kontext faktury zákazníka</p><p>Kontextový model faktury zákazníka – kontext faktury projektu</p> |
    | Norská elektronická faktura (NO)    | <p>Prodejní faktura</p><p>Faktura projektu</p> | <p>Kontextový model faktury zákazníka – kontext faktury zákazníka</p><p>Kontextový model faktury zákazníka – kontext faktury projektu</p> |
    | Španělská elektronická faktura (ES)      | <p>Prodejní faktura</p><p>Faktura projektu</p> | <p>Kontextový model faktury zákazníka – kontext faktury zákazníka</p><p>Kontextový model faktury zákazníka – kontext faktury projektu</p> |
    | Elektronická faktura PEPPOL            | <p>Prodejní faktura</p><p>Faktura projektu</p> | <p>Kontextový model faktury zákazníka – kontext faktury zákazníka</p><p>Kontextový model faktury zákazníka – kontext faktury projektu</p> |
    | Saúdskoarabská elektronická faktura (SA)| <p>Prodejní faktura</p><p>Faktura projektu</p> | <p>Kontextový model faktury zákazníka – kontext faktury zákazníka</p><p>Kontextový model faktury zákazníka – kontext faktury projektu</p> |

7. U každého názvu tabulky a kontextu vyberte a zadejte hodnotu mapování obchodního dokumentu podle následující tabulky.

    | Název funkce                         | Obchodní dokument | Mapování obchodního dokumentu |
    |--------------------------------------|-------------------|---------------------------|
    | Rakouské elektronické faktury (AT)    | <p>Prodejní faktura</p><p>Faktura projektu</p> | <p>Mapování modelu faktury – faktura zákazníka</p><p>Mapování modelu faktury – faktura projektu</p> |
    | Belgická elektronická faktura (BE)      | <p>Prodejní faktura</p><p>Faktura projektu</p> | <p>Mapování modelu faktury – faktura zákazníka</p><p>Mapování modelu faktury – faktura projektu</p> |
    | Brazilský NF-e (BR)                  | <p>Daňový doklad</p><p>Dopis o opravě</p> | <p>Mapování fiskálních dokumentů – Mapování fiskálních dokumentů</p><p>Mapování fiskálních dokumentů – mapování opravných dopisů</p> |
    | Brazilian NFS-e ABRASF Curitiba (BR) | Fiskální dokument služby | Mapování fiskálních dokumentů – Mapování fiskálních dokumentů |
    | Dánská elektronická faktura (DK)       | <p>Prodejní faktura</p><p>Faktura projektu</p> | <p>Mapování modelu faktury – faktura zákazníka</p><p>Mapování modelu faktury – faktura projektu</p> |
    | Egyptská elektronická faktura (EG)     | <p>Prodejní faktura</p><p>Faktura projektu</p> | <p>Mapování modelu faktury – faktura zákazníka</p><p>Mapování modelu faktury – faktura projektu</p> |
    | Estonská elektronická faktura (EE)     | <p>Prodejní faktura</p><p>Faktura projektu</p> | <p>Mapování modelu faktury – faktura zákazníka</p><p>Mapování modelu faktury – faktura projektu</p> |
    | Finská elektronická faktura (FI)       | <p>Prodejní faktura</p><p>Faktura projektu</p> | <p>Mapování modelu faktury – faktura zákazníka</p><p>Mapování modelu faktury – faktura projektu</p> |
    | Francouzská elektronická faktura (FR)       | <p>Prodejní faktura</p><p>Faktura projektu</p> | <p>Mapování modelu faktury – faktura zákazníka</p><p>Mapování modelu faktury – faktura projektu</p> |
    | Německá elektronická faktura (DE)       | <p>Prodejní faktura</p><p>Faktura projektu</p> | <p>Mapování modelu faktury – faktura zákazníka</p><p>Mapování modelu faktury – faktura projektu</p> |
    | FatturaPA (IT)                       | <p>Prodejní faktura</p><p>Faktura projektu</p> | <p>Mapování modelu faktury – faktura zákazníka</p><p>Mapování modelu faktury – faktura projektu</p> |
    | Mexická CFDI Interfactura (MX)       | <p>Prodejní faktura</p><p>Dodací list</p><p>Převod zásob</p><p>Doplněk platby</p> | Mapování modelu faktury – faktura zákazníka |
    | Nizozemská elektronická faktura (NL)        | <p>Prodejní faktura</p><p>Faktura projektu</p> | <p>Mapování modelu faktury – faktura zákazníka</p><p>Mapování modelu faktury – faktura projektu</p> |
    | Norská elektronická faktura (NO)    | <p>Prodejní faktura</p><p>Faktura projektu</p> | <p>Mapování modelu faktury – faktura zákazníka</p><p>Mapování modelu faktury – faktura projektu</p> |
    | Španělská elektronická faktura (ES)      | <p>Prodejní faktura</p><p>Faktura projektu</p> | <p>Mapování modelu faktury – faktura zákazníka</p><p>Mapování modelu faktury – faktura projektu</p> |
    | Elektronická faktura PEPPOL            | <p>Prodejní faktura</p><p>Faktura projektu</p> | <p>Mapování modelu faktury – faktura zákazníka</p><p>Mapování modelu faktury – faktura projektu</p> |
    | Saúdskoarabská elektronická faktura (SA)| <p>Prodejní faktura</p><p>Faktura projektu</p> | <p>Mapování modelu faktury – faktura zákazníka</p><p>Mapování modelu faktury – faktura projektu</p> |


## <a name="country-specific-configuration-of-application-setup"></a>Konfigurace nastavení aplikace pro určitou zemi

V závislosti na zemi nebo regionu může nastavení aplikace vyžadovat specifickou konfiguraci. 

Konkrétní kroky najdete v dokumentaci „Začínáme“, která je k dispozici pro vaši zemi nebo region.

## <a name="deploy-the-electronic-invoicing-feature-to-service-environment"></a>Nasazení funkce elektronické fakturace do prostředí služby

1. Na kartě **Verze** vyberte verzi funkce elektronické fakturace, kterou chcete nasadit.
2. Vyberte **Změnit stav** \> **Dokončeno**.
3. Vyberte **Změnit stav** \> **Publikovat**.
4. Vyberte **Nasadit**.
5. Nastavte možnost **Nasadit do připojené aplikace** na **Ne**.
6. Nastavte možnost **Nasadit do prostředí služby** na **Ano**.
7. V poli **Prostředí služby** vyberte prostředí služby elektronické fakturace, kam chcete nasadit funkci elektronické fakturace.
8. V poli **Od data** vyberte datum, kdy musí funkce elektronické fakturace nabýt účinnosti v Elektronické fakturaci.
9. Vyberte **OK**.

## <a name="deploy-the-electronic-invoicing-feature-to-connected-application"></a>Nasazení funkce elektronické fakturace do připojené aplikace

1. Na kartě **Verze** vyberte verzi funkce elektronické fakturace, kterou chcete nasadit.
2. Vyberte **Nasadit**.
3. Nastavte možnost **Nasadit do připojené aplikace** na **Ano**.
4. V poli **Připojit aplikaci** vyberte připojení, které je spojeno s vaší instancí Finance nebo Supply Chain Management.
5. Nastavte možnost **Nasadit do prostředí služby** na **Ne**.
6. Vyberte **OK**.

## <a name="turn-on-the-electronic-invoicing-feature-in-finance-or-supply-chain-management"></a>Zapnutí funkce elektronické fakturace ve Finance nebo Supply Chain Management

1. Přihlaste se k Finance nebo Supply Chain Management a ověřte si, že jste ve správné právnické osobě.
2. Přejděte na **Správa organizace** \> **Nastavení** \> **Parametry elektronického dokumentu**.
3. Na kartě **Funkce** vyberte funkci specifickou pro danou zemi/oblast a zapněte funkci elektronické fakturace pro Finance nebo Supply Chain Management. V následující tabulce je uveden seznam funkcí elektronické fakturace, které jsou k dispozici pro konkrétní zemi/oblasti. 

    | Název funkce                                          | Země nebo oblast  |
    |-------------------------------------------------------|-----------------|
    | Rakouské elektronické faktury (AT)                     | Rakousko         |
    | Belgická elektronická faktura (BE)                       | Belgie         |
    | Mexická elektronická faktura CFDI (MX)                  | Mexiko          |
    | Dánská elektronická faktura (DK)                        | Dánsko         |
    | Nizozemská elektronická faktura (NL)                         | Nizozemsko |
    | Egyptská elektronická faktura (EG)                      | Egypt           |
    | Estonská elektronická faktura (EE)                      | Estonsko         |
    | Finská elektronická faktura (FI)                       | Finsko         |
    | Francouzská elektronická faktura (FR)                        | Francie          |
    | Německá elektronická faktura (DE)                        | Německo         |
    | Italská elektronická faktura (IT)                       | Itálie           |
    | Brazilská elektronická faktura NF-e Federal (BR)      | Brazílie          |
    | NFS-e – elektronické faktura za služby (městské) pro Brazílii   | Brazílie          |
    | Norská elektronická faktura (NO)                     | Norsko          |
    | Elektronická faktura PEPPOL                             | Globální          |
    | Španělská elektronická faktura (ES)                       | Španělsko           |
    | Saúdskoarabská elektronická faktura (SA)                 | Saúdskoarabské království    |
    

4. Zvolte možnost **Uložit**.

## <a name="issue-electronic-invoices"></a>Vydávání elektronických faktur

1. Přejděte na **Správa organizace** \> **Periodické** \> **Elektronické dokumenty** \> **Odesílat elektronické dokumenty**.
2. Na pevné záložce **záznamy, které mají být zahrnuty** vyberte možnost **Filtr**.
3. Vybrat **Přidat** pro přidání názvu tabulky do filtru dotazu.
4. Vyberte tabulku, která obsahuje faktury.

    > [!NOTE]
    > Název tabulky musí být uveden v tabulce v části [Konfigurace nastavení aplikace](#configure-the-application-setup) dříve v tomto tématu.

5. Z tabulky, které se chcete dotazovat, vyberte název pole.
6. Zadejte název tabulky a název pole pro kritéria dotazování.
7. Opakováním kroků 5 a 6 přidejte do dotazu další pole a kritéria a poté vyberte **OK**.
8. Vyberte **OK**.

## <a name="view-submission-logs"></a>Zobrazit protokoly odeslání

1. Přejděte na **Správa organizace** \> **Periodické** \> **Elektronické dokumenty** \> **Protokol o odeslání elektronických dokumentů**.
2. V poli **Typ dokumentu** vyberte tabulku, která obsahuje faktury.

    > [!NOTE]
    > Název tabulky musí být uveden v tabulce v části [Konfigurace nastavení aplikace](#configure-the-application-setup) dříve v tomto tématu.

3. Vyberte fakturu v mřížce a poté vyberte **Dotaz** \> **Podrobnosti o podání**.


## <a name="related-topics"></a>Související témata

- [Přehled elektronické fakturace](e-invoicing-service-overview.md)
- [Začínáme se správou služby Elektronické fakturace](e-invoicing-get-started-service-administration.md)
- [Začínáme s Elektronickou fakturací pro Brazílii](e-invoicing-bra-get-started.md)
- [Začínáme s Elektronickou fakturací pro Mexiko](e-invoicing-mex-get-started.md)
- [Začněte s elektronickou fakturací pro Itálii](e-invoicing-ita-get-started.md)
- [Elektronické faktury zákazníka v Egyptě](emea-egy-e-invoices.md)
- [Elektronické faktury zákazníka v Saúdské Arábii](emea-sau-e-invoices.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
