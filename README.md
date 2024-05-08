# Screen-time-analysis

import pandas as pd
import numpy as np
import plotly.express as px
import plotly.graph_objects as go

data = pd.read_csv("/content/Screentime-App-Details-Dataset[1].csv")
figure = px.bar(data_frame=data, x="Date", y="Notifications", color="App",
title="NOTIFICATIONS Graph by DIVYANSHU SINGH")
figure.show()

figure = px.scatter(data_frame=data, x="Notifications", y="Usage",size="Notifications", trendline="ols", title="Relationship Between Number of Notification and amount of usage")
figure.show()
