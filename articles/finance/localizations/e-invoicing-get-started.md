---
title: Začněte s doplňkem elektronické fakturace
description: Toto téma poskytuje informace, které vám pomohou začít s doplňkem elektronické fakturace v Microsoft Dynamics 365 Finance a Dynamics 365 Supply Chain Management.
author: gionoder
manager: AnnBe
ms.date: 02/03/2021
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
ms.openlocfilehash: 07954c5c96f390bc651794f8b6c61f2a1a17ab8b
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/03/2021
ms.locfileid: "5111213"
---
# <a name="get-started-with-the-electronic-invoicing-add-on"></a>Začněte s doplňkem elektronické fakturace

[!include [banner](../includes/banner.md)]

Toto téma poskytuje informace, které vám pomohou začít s doplňkem elektronické fakturace.

V následující tabulce jsou uvedeny funkce elektronické fakturace a obchodní dokumenty, na které je lze použít.

| Název funkce                         | Obchodní dokument |
|--------------------------------------|-------------------|
| Rakouské elektronické faktury (AT)    | <p>Prodejní faktura</p><p>Faktura projektu</p> |
| Belgická elektronická faktura (BE)      | <p>Prodejní faktura</p><p>Faktura projektu</p> |
| Brazilský NF-e (BR)                  | <p>Model 55 fiskálního dokumentu</p><p>Dopis o opravě</p> |
| Brazilian NFS-e ABRASF Curitiba (BR) | Fiskální dokument služby |
| Brazilský NFS-e São Paulo (BR)       | Fiskální dokument služby |
| Dánská elektronická faktura (DK)       | <p>Prodejní faktura</p><p>Faktura projektu</p> |
| Egyptská elektronická faktura (EG)     | <p>Prodejní faktura</p><p>Faktura projektu</p> |
| Estonská elektronická faktura (EE)     | <p>Prodejní faktura</p><p>Faktura projektu</p> |
| Finská elektronická faktura (FI)       | <p>Prodejní faktura</p><p>Faktura projektu</p> |
| Francouzská elektronická faktura (FR)       | <p>Prodejní faktura</p><p>Faktura projektu</p> |
| Německá elektronická faktura (DE)       | <p>Prodejní faktura</p><p>Faktura projektu</p> |
| FatturaPA (IT)                       | <p>Prodejní faktura</p><p>Faktura projektu</p> |
| Mexická CFDI Interfactura (MX)       | <p>Prodejní faktura</p><p>Dodací list</p><p>Převod zásob</p><p>Doplněk platby</p> |
| Nizozemská elektronická faktura (NL)        | <p>Prodejní faktura</p><p>Faktura projektu</p> |
| Norská elektronická faktura (NO)    | <p>Prodejní faktura</p><p>Faktura projektu</p> |
| Španělská elektronická faktura (ES)      | <p>Prodejní faktura</p><p>Faktura projektu</p> |
| Elektronická faktura PEPPOL            | <p>Prodejní faktura</p><p>Faktura projektu</p> |

## <a name="prerequisites"></a>Předpoklady

Než provedete postupy v tomto tématu, musí být splněny následující předpoklady:

- Nakonfigurujte Regulatory Configuration Service (RCS) a prostředí Microsoft Dynamics 365 Finance nebo Dynamics 365 Supply Chain Management, abyste mohli odeslat doplněk elektronické fakturace.
- Vytvořte prostředí služby a publikujte jej do doplňku elektronické fakturace. Další informace viz [Začínáme se správou služby doplňku elektronické fakturace](e-invoicing-get-started-service-administration.md).
- Vytvoření propojené aplikace. Další informace viz [Začínáme se správou služby doplňku elektronické fakturace](e-invoicing-get-started-service-administration.md).
- Vytvořte poskytovatele konfigurace pro vaši organizaci. Další informace naleznete ve [Vytvoření poskytovatele konfigurace a jejich označení jako aktivních](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).

## <a name="import-an-electronic-invoicing-feature-from-the-microsoft-configuration-provider"></a>Importujte funkci elektronické fakturace od poskytovatele konfigurace společnosti Microsoft 

1. Přihlaste se ke svému účtu Regulatory Configuration Service (RCS).
2. V pracovním prostoru **Funkce globalizace** v části **Funkce** vyberte dlaždici **elektronická fakturace**.
3. Vyberte **Import** a potom vyberte **Synchronizovat**.
4. Filtrujte sloupec **Poskytovatel konfigurace** sloupec podle výrazu **Microsoft**.
5. Vyberte název funkce elektronické fakturace z tabulky na začátku tohoto tématu a poté vyberte **Import**.

## <a name="create-an-electronic-invoicing-feature-under-your-organization-provider"></a>Vytvoření funkce elektronické fakturace u poskytovatele organizace

1. V RCS v části **Funkce** pracovního prostoru **Funkce globalizace** vyberte dlaždici **elektronická fakturace**.
2. Vyberte **Přidat** > **Na základě stávající funkce** a do pole **Název** zadejte název funkce elektronické fakturace.
3. Do pole **Popis** zadejte popis funkce.
4. V **poli základní funkce** vyberte importovanou funkci elektronické fakturace od poskytovatele konfigurace společnosti Microsoft.
5. Vyberte **Vytvořit funkci**.

## <a name="configure-the-electronic-invoicing-feature"></a>Konfigurace funkce elektronické fakturace

V závislosti na zemi nebo regionu může funkce elektronické fakturace vyžadovat další konfiguraci. Konkrétní kroky najdete v dokumentaci „Začínáme“, která je k dispozici pro vaši zemi nebo region.

## <a name="configure-the-application-setup"></a>Konfigurace nastavení aplikace

1. Vyberte funkci elektronické fakturace, kterou jste vytvořili.
2. Na kartě **Verze** ověřte, že je vybrána verze **Koncept**.
3. Na kartě **Nastavení** vyberte **Nastavení aplikace**.

    > [!NOTE]
    > Ověřte, zda je vaše organizace nastavena jako **Aktivní** poskytovatel konfigurace. Další informace naleznete ve [Vytvoření poskytovatele konfigurace a jejich označení jako aktivních.](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).

4. Vyberte **Nastavení funkce** a potom vyberte **Připojená aplikace**.
5. V části **Typy elektronického dokumentu** vyberte **Přidat**.
6. U každého obchodního dokumentu, který funkce podporuje, vyberte a zadejte hodnotu **Název tabulky** podle následující tabulky.

    | Název funkce                         | Obchodní dokument | Název tabulky |
    |--------------------------------------|-------------------|------------|
    | Rakouské elektronické faktury (AT)    | <p>Prodejní faktura</p><p>Faktura projektu</p> | <p>Deník faktur odběratele</p><p>Faktura projektu</p> |
    | Belgická elektronická faktura (BE)      | <p>Prodejní faktura</p><p>Faktura projektu</p> | <p>Deník faktur odběratele</p><p>Faktura projektu</p> |
    | Brazilský NF-e (BR)                  | <p>Daňový doklad</p><p>Dopis o opravě</p> | Daňový doklad |
    | Brazilian NFS-e ABRASF Curitiba (BR) | Fiskální dokument služby | Daňový doklad |
    | Brazilský NFS-e São Paulo (BR)       | Fiskální dokument služby | Daňový doklad |
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

7. U každého obchodního dokumentu, který funkce podporuje, vyberte a zadejte hodnotu **Kontext** podle následující tabulky.

    | Název funkce                         | Obchodní dokument | Kontext |
    |--------------------------------------|-------------------|---------|
    | Rakouské elektronické faktury (AT)    | <p>Prodejní faktura</p><p>Faktura projektu</p> | <p>Kontextový model faktury zákazníka – kontext faktury zákazníka</p><p>Kontextový model faktury zákazníka – kontext faktury projektu</p> |
    | Belgická elektronická faktura (BE)      | <p>Prodejní faktura</p><p>Faktura projektu</p> | <p>Kontextový model faktury zákazníka – kontext faktury zákazníka</p><p>Kontextový model faktury zákazníka – kontext faktury projektu</p> |
    | Brazilský NF-e (BR)                  | <p>Daňový doklad</p><p>Dopis o opravě</p> | <p>Kontextový model faktury zákazníka – kontext fiskálního dokumentu</p><p>Kontextový model faktury zákazníka – kontext dopisu opravy FD</p> |
    | Brazilian NFS-e ABRASF Curitiba (BR) | Fiskální dokument služby| Kontextový model faktury zákazníka – kontext fiskálního dokumentu |
    | Brazilský NFS-e São Paulo (BR)       | Fiskální dokument služby| Kontextový model faktury zákazníka – kontext fiskálního dokumentu |
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

8. U každého obchodního dokumentu, který funkce podporuje, vyberte a zadejte hodnotu **Mapování obchodního dokumentu** podle následující tabulky.

    | Název funkce                         | Obchodní dokument | Mapování obchodního dokumentu |
    |--------------------------------------|-------------------|---------------------------|
    | Rakouské elektronické faktury (AT)    | <p>Prodejní faktura</p><p>Faktura projektu</p> | <p>Mapování modelu faktury – faktura zákazníka</p><p>Mapování modelu faktury – faktura projektu</p> |
    | Belgická elektronická faktura (BE)      | <p>Prodejní faktura</p><p>Faktura projektu</p> | <p>Mapování modelu faktury – faktura zákazníka</p><p>Mapování modelu faktury – faktura projektu</p> |
    | Brazilský NF-e (BR)                  | <p>Daňový doklad</p><p>Dopis o opravě</p> | <p>Mapování fiskálních dokumentů – Mapování fiskálních dokumentů</p><p>Mapování fiskálních dokumentů – mapování opravných dopisů</p> |
    | Brazilian NFS-e ABRASF Curitiba (BR) | Fiskální dokument služby | Mapování fiskálních dokumentů – Mapování fiskálních dokumentů |
    | Brazilský NFS-e São Paulo (BR)       | Fiskální dokument služby | Mapování fiskálních dokumentů – Mapování fiskálních dokumentů |
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

V závislosti na zemi nebo regionu může funkce elektronické fakturace vyžadovat další konfiguraci. Konkrétní kroky najdete v dokumentaci „Začínáme“, která je k dispozici pro vaši zemi nebo region.

## <a name="deploy-the-electronic-invoicing-feature"></a>Nasazení funkce elektronické fakturace

1. Na kartě **Verze** vyberte verzi funkce elektronické fakturace, kterou chcete nasadit.
2. Vyberte **Změnit stav** \> **Dokončeno**.
3. Vyberte **Změnit stav** \> **Publikovat**.
4. Vyberte **Nasadit**.
5. Nastavte možnost **Nasadit do připojené aplikace** na **Ano**.
6. Na stránce **Připojit aplikaci** vyberte připojení, které je spojeno s vaší instancí Finance nebo Supply Chain Management.
7. Nastavte možnost **Nasadit do prostředí služby** na **Ano**.
8. V poli **Prostředí služby** vyberte prostředí služby doplňku elektronické fakturace, kam chcete nasadit funkci elektronické fakturace.
9. V poli **Od data** vyberte datum, kdy musí funkce elektronické fakturace nabýt účinnosti v doplňku elektronické fakturace.
10. Vyberte **OK**.

## <a name="turn-on-the-electronic-invoicing-feature-in-finance-or-supply-chain-management"></a>Zapnutí funkce elektronické fakturace ve Finance nebo Supply Chain Management

1. Přihlaste se k Finance nebo Supply Chain Management a ověřte si, že jste ve správné právnické osobě.
2. Přejděte na **Správa organizace** \> **Nastavení** \> **Parametry elektronického dokumentu**.
3. Na kartě **Funkce** vyberte záložku funkce nebo odkazy uvedené v následující tabulce, chcete-li zapnout funkci elektronické fakturace pro Finance nebo Supply Chain Management.

    | Název funkce                         | Země nebo oblast  | Odkaz na funkci |
    |--------------------------------------|-----------------|-------------------|
    | Rakouské elektronické faktury (AT)    | Rakousko         | EUR-00023 |
    | Belgická elektronická faktura (BE)      | Belgie         | EUR-00023 |
    | Brazilský NF-e (BR)                  | Brazílie          | BR-00053 |
    | Brazilian NFS-e ABRASF Curitiba (BR) | Brazílie          | BR-00095 |
    | Brazilský NFS-e São Paulo (BR)       | Brazílie          | BR-00095 |
    | Dánská elektronická faktura (DK)       | Dánsko         | <p>EUR-00023</p><p>DK-00001</p> |
    | Nizozemská elektronická faktura (NL)        | Nizozemsko | EUR-00023 |
    | Egyptská elektronická faktura (EG)     | Egypt           | EG-00008 |
    | Estonská elektronická faktura (EE)     | Estonsko         | EUR-00023 |
    | Finská elektronická faktura (FI)      | Finsko         | EUR-00023 |
     Francouzská elektronická faktura (FR)       | Francie           | EUR-00023 |
    | Německá elektronická faktura (DE)       | Německo         | EUR-00023 |
    | Mexická CFDI Interfactura (MX)       | Mexiko          | <p>MX-00010</p><p>MX-00016</p> |
    | Norská elektronická faktura (NO)    | Norsko          | <p>EUR-00023</p><p>NO-00010</p> |
    | Španělská elektronická faktura (ES)      | Španělsko           | <p>EUR-00023</p><p>ES-00025</p> |
    | Italská elektronická faktura (IT)      | Itálie           | <p>EUR-00023</p><p>IT-00036</p> |
    | Elektronická faktura PEPPOL            | Evropa          | EUR-00023 |

4. Zvolte **Uložit**.

## <a name="issue-electronic-invoices"></a>Vydávání elektronických faktur

1. Přejděte na **Správa organizace** \> **Periodické** \> **Elektronické dokumenty** \> **Odesílat elektronické dokumenty**.
2. Na pevné záložce **Záznam, který má být zahrnut** vyberte možnost **Filtr**.
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

V závislosti na zemi nebo regionu může funkce elektronické fakturace vyžadovat další konfiguraci. Konkrétní kroky najdete v dokumentaci „Začínáme“, která je k dispozici pro vaši zemi nebo region.

## <a name="related-topics"></a>Související témata

- [Přehled doplňku elektronické fakturace](e-invoicing-service-overview.md)
- [Začněte s doplňkem elektronické fakturace pro Brazílii](e-invoicing-bra-get-started.md)
- [Začněte s doplňkem elektronické fakturace pro Mexiko](e-invoicing-mex-get-started.md)
- [Začněte s doplňkem elektronické fakturace pro Itálii](e-invoicing-ita-get-started.md)
- [Elektronické faktury zákazníka v Egyptě](emea-egy-e-invoices.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]