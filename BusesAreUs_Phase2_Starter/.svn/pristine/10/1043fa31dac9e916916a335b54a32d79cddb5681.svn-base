package ca.ubc.cs.cpsc210.translink.providers;

import ca.ubc.cs.cpsc210.translink.model.Stop;

import java.io.IOException;
import java.net.MalformedURLException;
import java.net.URL;

/**
 * Wrapper for Translink Arrival Data Provider
 */
public class HttpArrivalDataProvider extends AbstractHttpDataProvider {
    private Stop stop;

    public HttpArrivalDataProvider(Stop stop) {
        super();
        this.stop = stop;
    }

    @Override
    /**
     * Produces URL used to query Translink web service for expected arrivals at
     * the stop specified in call to constructor.
     *
     * @returns URL to query Translink web service for arrival data
     *
     *
     * API KEY:        YLu122V1JXEbJWYyqpwd
     */
    // Design a function to retrieve URL from API
    protected URL getURL() throws MalformedURLException {
        String KEY = "YLu122V1JXEbJWYyqpwd";
        Integer stopNumber = stop.getNumber();
        String stopNumberToString = Integer.toString(stopNumber);
        URL websiteURL = new URL("http://api.translink.ca/rttiapi/v1/stops/" + stopNumberToString + "/estimates?apikey=" + KEY);
        return websiteURL;
    }

    @Override
    public byte[] dataSourceToBytes() throws IOException {
        return new byte[0];
    }
}
